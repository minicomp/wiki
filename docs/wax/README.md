# Minicomp/Wax

## About

Wax is an extensible workflow and 'unplatform' for producing __scholarly exhibitions__ with [minimal computing](http://go-dh.github.io/mincomp/) principles.

## Demo site

The best way to get started with
## Wax theme

## Wax tasks

Wax Tasks is a gem-packaged set of [Rake](https://ruby.github.io/rake/) tasks for creating minimal exhibitions with [Jekyll](https://jekyllrb.com/), [IIIF](http://iiif.io), and [ElasticLunr.js](http://elasticlunr.com/). These tasks are the muscle behind [Wax](/wax/)—building search indexes, generating pages, running tests and more behind the scenes.

You might be wondering, *what's Rake?* The short answer is a Ruby task management/automation tool like [Make](). It lets you run commands easily with snappy names, which makes it perfect for performing the discrete actions Wax needs. Each task can be called with the prefix of `$ bundle exec rake [task]`. For Wax Tasks, each task starts with `wax:`, as in `$ bundle exec rake wax:pagemaster` or `$ bundle exec rake wax:test`.

You might also be wondering *if Wax uses Jekyll, why aren't these tasks Jekyll plugins instead?* By using Rake, we can separate functionality from the Jekyll build process, making actions simpler and easier to maintain. One bonus is that you can easily write your own Rake tasks to interface with Wax Tasks, and another is that you can still use GitHub pages. Lastly, you aren't tied to using the Wax Theme or any other theme in particular; you can readily grab `_includes` and `_layouts` from wherever you like, since the tasks are for generating/transforming data, not displaying it.

### Getting Started

#### Prerequisites

You'll need `Ruby >= 2.2` with `bundler` installed. Check your versions with:
```bash
$ ruby -v
  ruby 2.4.2p198 (2017-09-14 revision 59899) [x86_64-darwin15]

$ bundler -v
  Bundler version 1.16.1
```
> Stuck with an earlier system Ruby and don't know where to start? This [guide](https://learn.cloudcannon.com/jekyll/install-jekyll-on-linux/) is a good one. Side note: Windows does not play particularly nicely with Jekyll. It is strongly recommended you use a Unix machine running Linux/Ubuntu/Mac, but do what you must!

To use the IIIF task, you will also need to have ImageMagick installed and functional. You can check to see if you have ImageMagick by running:
```bash
$ convert -version
  Version: ImageMagick 6.9.9-20 Q16 x86_64 2017-10-15 http://www.imagemagick.org
  Copyright: © 1999-2017 ImageMagick Studio LLC
  License: http://www.imagemagick.org/script/license.php
  Features: Cipher DPC Modules
  Delegates (built-in): bzlib freetype jng jpeg ltdl lzma png tiff xml zlib
```

You can learn more about installing ImageMagick (e.g., for [mac](http://macappstore.org/imagemagick/) or [ubuntu](https://www.tutorialspoint.com/articles/how-to-install-imagemagick-on-ubuntu)) or ignore this completely if you do not plan to generate IIIF derivatives.

#### Installing

Once you've got a modern Ruby and Bundler set up, you can add `wax_tasks` to your Jekyll site's Gemfile:

```ruby
gem 'wax_tasks'
```

... and install with bundler:

```bash
$ bundle install
```

Next, create a `Rakefile` in the root of your site with the following content:
```ruby
spec = Gem::Specification.find_by_name 'wax_tasks'
Dir.glob("#{spec.gem_dir}/lib/tasks/*.rake").each {|r| load r}
```

This tells Bundler how to find and run the tasks. Test that you have them available with: `$ bundle exec rake --tasks`. You should see:
```bash
$ bundle exec rake --tasks

rake wax:ghbranch    # build site with gh-baseurl and publish to gh-pages b...
rake wax:jspackage   # write a simple package.json
rake wax:lunr        # build lunr search index
rake wax:pagemaster  # generate collection md pages from yaml or csv data s...
rake wax:s3branch    # build site with baseurl and publish to s3 branch
rake wax:test        # run htmlproofer, rspec if exists
```

That's it!

> Don't have a Jekyll site yet? Follow [these steps](https://jekyllrb.com/docs/quickstart/) to make one or, better yet, clone the [Wax demo](https://github.com/minicomp/wax) which comes with `wax_tasks`.

### The Tasks

After following the installation instructions above, you will have access to the rake tasks in your shell by running `$ bundle exec rake wax:taskname` in the root directory of your Jekyll site.

The current tasks available include:


#### wax:pagemaster

Takes a CSV, YAML, or JSON file of collection records and generates a Markdown page for each one using a specified layout.

[Read More](/wax/tasks/pagemaster#top).

#### wax:lunr

Generates a client-side JSON search index of your site for use with [ElasticLunr.js](http://elasticlunr.com/).

[Read More](/wax/tasks/lunr#top).

#### wax:iiif

Takes a local directory of images and generates tiles and data that work with a IIIF compliant image viewer like [OpenSeaDragon](https://openseadragon.github.io/), [Mirador](http://projectmirador.org/), or [Leaflet IIIF](https://github.com/mejackreed/Leaflet-IIIF).

[Read More](/wax/tasks/iiif#top).

#### wax:test

Runs [htmlproofer](https://github.com/gjtorikian/html-proofer) on your compiled site to look for broken links, HTML errors, and accessibility concerns. Runs [Rspec](http://rspec.info/) tests if a `.rspec` file is present.

[Read More](/wax/tasks/test#top).


#### Extra tasks

These include `wax:push:gh` and `wax:pushs3` (which push the compiled exhibition site to the `gh-pages` and `s3` branches of your repository respectively for deployment) and `wax:jspackage` (which creates a dummy `package.json` file to track your JavaScript dependencies.)

[Read More](/wax/tasks/extras#top)
