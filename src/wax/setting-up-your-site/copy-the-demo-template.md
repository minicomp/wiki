---
layout: default
title: Copy the demo template
nav_order: 1
parent: Setting up your site
grand_parent: Wax
permalink: /wax/setting-up-your-site/downloading-the-demo/
---

# {{ page.title }}

1. Log into your [GitHub account](https://github.com/). (Or sign up if you don't have one!)

2. Head to the [Wax demo page](https://github.com/) and click **"Use this Template"** button. It will prompt you to create a copy of the repository in your own account. You should name it after the collection or exhibition you'll make, since this name will inform your free URL for the project with GitHub. For this example, our repository is called **"my-wax-site"**.

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

7. Install the project-specific Ruby dependencies by running the command
  ```sh
  bundle install
  ```

That's it!
