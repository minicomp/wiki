require 'dotenv'
require 'html-proofer'
require 'json'
require 'octokit'
require 'yaml'

Dotenv.load

@config  = YAML.load_file '_config.yml'
@baseurl = ENV['BASEURL'] || @config.dig('baseurl')

task :test do
  Rake::Task["reset"].invoke
  sh "bundle exec jekyll build -b '#{@baseurl}' -d '_site#{@baseurl}'"
  opts = {
    disable_external: true,
    ignore_urls: [/elasticlunr/]
  }
  HTMLProofer.check_directory('./_site', opts).run
end

task :reset do
  sh "rm -rf _site .jekyll*"
end

task :build do
  Rake::Task["octokit"].invoke
  sh "bundle exec jekyll build -b '#{@baseurl}'"
end

task :octokit do
  @file   = './src/_data/contributors.json'
  @client = ENV['TOKEN'].nil? ?
    Octokit::Client.new :
    Octokit::Client.new(access_token: ENV['TOKEN'])
  @users = {}
  @repos = @client.org_repos('minicomp').map(&:full_name)
  @repos.each do |repo|
    @client.contribs(repo).each do |user|
      next if user.type == 'Bot' or user.login == 'gitter-badger'
      if @users.key? user.login
        @users[user.login][:contributions] ||= 0
        @users[user.login][:contributions] += user.contributions
      else
        @users[user.login] = {
          contributions: user.contributions,
          avatar_url: user.avatar_url
        }
      end
    end
    issues = @client.list_issues(repo, state: 'all').group_by { |i| i.user.login }
    issues.each do |user, user_issues|
      next if user.include? '[bot]'
      if @users.key? user
        @users[user][:issues] ||= 0
        @users[user][:issues] += user_issues.length
      else
        @users[user] = {
          issues: user_issues.length,
          avatar_url: user_issues.first.user.avatar_url
        }
      end
    end
  end
  @data = @users.sort_by { |_k, v| -v.fetch(:contributions, 0) }.to_h

  File.open(@file, 'w') { |f| f.write JSON.pretty_generate(@data) }
end
