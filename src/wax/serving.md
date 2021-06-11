---
layout: default
title: Serving your site
nav_order: 8
parent: Wax
permalink: /wax/serving/
---

# {{ page.title }}

## Serving locally for development

If you're running Wax directly on your machine, serving
\*should\* be as simple as

```sh
bundle exec jekyll serve
```

If you're in a Docker container, you'll need to specify the host:

```sh
bundle exec jekyll serve --host 0.0.0.0
```

## Hosting remotely

There are many options. Our demo uses GitHub pages. You can also use FTP deployment to a server or sync files to an S3 or Min.io bucket.

Have you used these options and would like to share a "recipe" for our Wiki? Please ping us on the [Code4Lib Slack](https://docs.google.com/forms/d/e/1FAIpQLSeD77mBp0Y13mFePF8UmDwFrlbxNx3VttEjz_3dgglJeK-Zbg/viewform?c=0&w=1)!
