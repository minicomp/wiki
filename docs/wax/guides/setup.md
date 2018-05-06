[![logo](./../../assets/logo.png)](/)

# Setting up your System

### Ruby

You'll need `Ruby >= 2.2` with `bundler` installed. Check your versions with:
```bash
$ ruby -v
  ruby 2.4.2p198 (2017-09-14 revision 59899) [x86_64-darwin15]

$ bundler -v
  Bundler version 1.16.1
```
> Stuck with an earlier system Ruby and don't know where to start? This [guide](https://learn.cloudcannon.com/jekyll/install-jekyll-on-linux/) is a good one. Side note: Windows does not play particularly nicely with Jekyll. It is strongly recommended you use a Unix machine running Linux/Ubuntu/Mac, but do what you must!

### ImageMagick

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

### Git

Make sure you have Git installed and configured correctly:

```bash
$ git --version
  git version 2.15.1
```

Clone the demo repository:

```bash
$ git clone https://github.com/minicomp/wax.git && cd wax
```

Install the Ruby dependencies with Bundler:

```bash
$ bundle install
```
 Make sure the demo builds as is:
 ```bash
 $ bundle exec jekyll build --verbose
 ```

### Next:

> [Preparing your data and metadata](/wax/guides/data#top)
