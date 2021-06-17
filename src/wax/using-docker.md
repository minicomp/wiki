---
layout: default
title: Using Docker
nav_order: 9
parent: Wax
permalink: /wax/using-docker/
---

# {{ page.title }}

Using Docker to install and run the software behind Wax can be a convenient strategy. To do so, you'll need to first follow the steps on our [Docker installation guide](../setting-up-your-system/with-docker/).

Next, complete the steps 1-6 on [Copying the Demo template](../setting-up-your-site/copy-the-demo-template/). Instead of running `bundle install` you should:

1. Make sure you are inside your cloned repository (from [Copying the Demo template](../setting-up-your-site/copy-the-demo-template/)). You can check where you are by running:
  ```sh
  pwd
  ```

2. Build the minicomp/wax base Docker image:
  ```sh
  docker build -t minicomp/wax .
  ```
#### \***Note:** Make sure you copy the whole command above, including the "." at the end!
<br>

3. Create and access an interactive bash container from the image by running:
  ```sh
  docker run -it --rm -v ${PWD}:/wax --name wax -p 4000:4000 minicomp/wax bash minicomp/wax bash
  ```
4. **Inside the container**, update the dependencies by running:
  ```sh
  bundle update
  ```
5. Check that you have the wax_tasks available by running:
  ```sh
  bundle exec rake --tasks
  ```

**Whenever you're running Wax's tasks to process collection data or running Jekyll to serve your site, you'll have to do so from within this container.**

You can exit any time by typing the command `exit`, which will destroy the container but not the base image. Create and access a new one as needed by running the command starting with `docker run ...` above.

#### \***Note:** Make sure you use Git commands *outside* the container, on your host computer!
