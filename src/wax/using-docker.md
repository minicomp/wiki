---
layout: default
title: Using Docker
nav_order: 9
parent: Wax
permalink: /wax/using-docker/
---

# {{ page.title }}

Using Docker to install and run the software behind Wax can be a convenient strategy. To do so, you'll need to first follow the steps on our [Docker installation guide](../setting-up-your-system/with-docker/).

Next, after completing the steps on [Copying the Demo template](../setting-up-your-site/copy-the-demo-template/), instead of running `bundle install` you should:

1. Build the minicomp/wax base Docker image:

```sh
docker build -t minicomp/wax .
```

2. Create and access an interactive bash container from the image by running:

```sh
docker run -it --rm -v "$PWD":/wax --name wax -p 4000:4000 minicomp/wax bash
```

Whenever you're running Wax's tasks to process collection data or running Jekyll to serve your site, you'll have to do so from within this container.

You can exit any time with `Control+C`, which will destroy the container but not the base image. Create and access a new one as needed by running Step 2 above.

#### \***Note:** Make sure you use Git commands *outside* the container, on your host computer!
