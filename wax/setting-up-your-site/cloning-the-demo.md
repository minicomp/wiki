---
layout: default
title: Cloning the demo
nav_order: 1
parent: Setting up your site
grand_parent: Wax
permalink: /wax/setting-up-your-site/cloning-the-demo/
---

# Cloning the demo

## Option 1. Download the demo for use with GitHub pages

1. Change directory into where you'd like your site, e.g., your Desktop:
    ```sh
    cd ~/Desktop
    ```
2. Clone the Wax demo repository from the `gh-pages` branch:
    ```sh
    git clone https://github.com/minicomp/wax.git -b 'gh-pages'
    ```
3. Change directory into the site repository and install the dependencies:
    ```sh
    cd wax
    bundle install
    ```
4. Serve the site locally
    ```sh
    bundle exec jekyll serve
    ```

## Option 2. Clone the demo without using GitHub pages

1. Change directory into where you'd like your site, e.g., your Desktop:
    ```sh
    cd ~/Desktop
    ```
2. Clone the Wax demo repository from the master branch:
    ```sh
    git clone https://github.com/minicomp/wax.git -b master
    ```
3. Change directory into the site repository and install the dependencies:
    ```sh
    cd wax
    bundle install
    ```
4. Serve the site locally
    ```sh
    bundle exec jekyll serve
    ```

When the demo site is serving correctly you're ready to swap in your own content and configuration to make your own exhibition site.
