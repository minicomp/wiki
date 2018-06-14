[![logo](./../assets/logo.png)](/)

# Minicomp/Wax

[![wax_screen](./../assets/wax_screen.gif)](https://minicomp.github.io/wax/)

> Live Wax Demo site: <https://minicomp.github.io/wax/>.<br>
> Wax Demo repository: <https://github.com.minicomp/wax/>.

# About

Wax is an extensible workflow for producing __scholarly exhibitions__ with [minimal computing](http://go-dh.github.io/mincomp/) principles. It focuses on a few key tasks for creating digital exhibitions as static sites, namely:

- generating pages for exhibition items from (meta)data files
- generating IIIF derivatives and JSON for deep-zooming viewers and interoperable image content
- generating a search index
- running tests to catch errors

Wax is comprised of a few Ruby gems, some customizable UI components, and a lot of documentation/recipes for use using them to create, deploy, and maintain digital exhibitions.

# Who is it for?

Wax is for individuals and groups who either don't have or don't want to use a lot of resources to create scholarly exhibitions. It's best suited for folks who are willing to take on some technical responsibility in exchange for a lot of flexibility.

At the moment, Wax has a relatively high but general-purpose learning curve. To get the most out of Wax, you should have some familiarity with:

- Using an interactive shell (e.g., Bash/Terminal) to install and interact with programs and libraries on your local machine.
- Using Git and GitHub to version control and collaborate on projects
- Using Jekyll to generate static sites.
- Creating and normalizing data files (e.g., CSVs, JSOM, YAML)
- File-naming conventions and best practices
- Writing HTML, CSS, and some JavaScript

If you do not meet the requirements above, not to worry! There's a [guide](wax/guides/catchup#top) with resources to catch you up.

# Wax Demo

The easiest way to **get started** with your own Wax exhibition is **by cloning the [Minicomp/Wax repository](https://github.com/minicomp/wax)** and swapping out content, media, styles, and components **to make it your your own**. [Read the full guide.](#make-your-own-exhibition)

> Advanced users can check back to find a **Ruby gem / Jekyll theme** with the layouts, includes, and scripts from the demo.

# Issues / Contributing

The canonical source for Wax is the [Minicomp](https://github.com/minicomp/wax/) fork of the project. Please submit issues (bugs, feature requests, questions, etc.) as well as pull requests only to the Minicomp/Wax repository.

# Primary Tooling

Wax is a flexible workflow and not a platform. As such, its tooling is more of a dynamic roster than a stack. At its center are __[Jekyll](http://jekyllrb.com)__ and __[Wax Tasks](https://github.com/minicomp/wax_tasks/)__ (which are both Ruby gems), but the rest of the components
are purely optional depending on what you'd like to do and how you'd like to do it. The following list is by no means exhaustive, but gives an outline of Wax's open source super group:

__For searching/indexing:__
- [elasticlunr.js](http://elasticlunr.com/)

__For IIIF generation/presentation:__
- [wax_iiif gem](https://github.com/minicomp/wax_iiif/) (fork of [iiif_s3](https://github.com/cmoa/iiif_s3))
- [leaflet.js](http://leafletjs.com/) and [leaflet-iiif.js](https://github.com/mejackreed/Leaflet-IIIF)
- [imagemagick](https://www.imagemagick.org/script/index.php)

__For theming:__
- [jquery](http://jquery.com/)
- [bootstrap4](https://getbootstrap.com/docs/4.0/getting-started/introduction/)

__For testing:__
- [rspec gem](http://rspec.info/)
- [html-proofer gem](https://github.com/gjtorikian/html-proofer)
- [capybara gem](http://teamcapybara.github.io/capybara/)
- [travis-ci](https://travis-ci.org/)


# Quick Start

Make sure your system is ready with modern Ruby (>=2.2), git, and ImageMagick installed.

Install Bundler
```sh
$ gem install bundler
```
Clone the repository and change directory into it
```sh
$ git clone https://github.com/minicomp/wax.git && cd wax
```
Install the Ruby Dependencies
```sh
$ bundle install
```
Serve the site locally
```sh
$ bundle exec jekyll serve
```

# Make Your Own Exhibition

- [Setting up your system](wax/guides/setup#top)
- [Preparing your data and metadata](wax/guides/data#top)
- [Using Wax Tasks](wax/guides/tasks#top)
- [Using the components](wax/guides/components#top)
- [Useful links](wax/guides/links#top)
