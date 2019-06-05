---
layout: default
title: Setting up your system
nav_order: 1
has_children: true
parent: Wax
permalink: /wax/system-requirements/
---

# System requirements

You'll need __modern Ruby__ (`>=2.4`) with __Bundler__,  __Git__, __ImageMagick__, and __GhostScript__. You can check your versions with the steps below. If you don't have current versions for these packages, see our [Installation guide]( {{ '/wax/system-requirements/installation-guide/' | absolute_url }}).

Check for Ruby:

```sh
$ ruby -v
  ruby 2.4.2p198 (2017-09-14 revision 59899) [x86_64-darwin15]
```

Check for Bundler:

```sh
$ bundler -v
  Bundler version 1.16.1
```

Check for Git:

```sh
$ git --version
  git version 2.19.0
```

To process images, you will also need to have __ImageMagick__ and __Ghostscript__ installed and functional.

Check ImageMagick:

```sh
$ convert -version
  Version: ImageMagick 6.9.9-20 Q16 x86_64 2017-10-15 http://www.imagemagick.org
  Copyright: (c) 1999-2017 ImageMagick Studio LLC
```

Check Ghostscript:

```sh
$ gs -version
  GPL Ghostscript 9.21 (2017-03-16)
  Copyright (c) 2017 Artifex Software, Inc.  All rights reserved.
```

