---
layout: default
title: Copy the demo template
nav_order: 1
parent: Setting up your site
grand_parent: Wax
permalink: /wax/setting-up-your-site/copy-the-demo-template/
---

# {{ page.title }}

1. Log into your [GitHub account](https://github.com/). (Or sign up if you don't have one!)

2. Head to the [Wax repository](https://github.com/minicomp/wax) and click **"Use this Template"** button (Green). It will prompt you to create a copy of the repository in your own account. You should name it after the collection or exhibition you'll make, since this name will inform your free URL for the project with GitHub. For this example, our repository is called **"my-wax-site"**.

3. On your own, new Wax repository page, click the Green **"Code"** button and copy the URL it provides to your clipboard, e.g,
  ```sh
  git@github.com:mnyrop/my-wax-site.git
  ```

4. Open your Terminal/Shell application and change directory into where you'd like to work on your project, e.g., your Desktop:
  ```sh
  cd ~/Desktop
  ```

5. Run the `git clone` command plus the link you copied on your clipboard in one line, e.g.,
  ```sh
  git clone git@github.com:mnyrop/my-wax-site.git
  ```

6. When the clone is complete, change directory into your newly cloned project folder, in our case:
  ```sh
  cd my-wax-site
  ```

### If you installed manually:

<span style="display:none">\\</span>7. Install the project-specific Ruby dependencies by running the command<sup>*</sup>

  ```sh
  bundle install
  ```

#### \***Note:** If you're using Docker, you do not need to run step \#7. It is run for you whenever you run or enter the container.


### If you installed with Docker

<span style="display:none">\\</span>7. Follow the steps on the [Using Docker](../../using-docker/) quick reference to build your container.
