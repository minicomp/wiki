require 'html-proofer'

desc 'run htmlproofer, rspec if .rspec file exists'
task :test do
  `rm -rf _site`
  `bundle exec jekyll build -d _site/wiki`
  opts = {
    check_external_hash: true,
    allow_hash_href: true,
    check_html: true,
    empty_alt_ignore: true,
    only_4xx: true,
    verbose: true
  }
  HTMLProofer.check_directory('./_site', opts).run
  `rm -rf _site`
end
