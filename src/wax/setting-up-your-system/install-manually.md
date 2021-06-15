---
layout: page
title: Manual Installation Guide
nav_order: 1
parent: Setting up your system
grand_parent: Wax
permalink: /wax/setting-up-your-system/install-manually/
---
# {{ page.title }}
{: .no_toc }

Before starting with this guide, make sure this installation option makes the most sense for you by [reading about the Pros and Cons](../#guides).

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

## On Mac

1. First you'll want to install [Homebrew](https://brew.sh/). It'll make installing everything else easier.

    Check on your terminal to see you if you have Homebrew installed by running the command:
    ```sh
    brew -v
    ```

    If you don't have Homebrew, visit [the Homebrew site](https://brew.sh/) and follow their installation instructions. In the process of installing Homebrew, you may get asked to install XCode Command Line Tools. Say yes.


2. After you have Homebrew, install Git and Gnupg by running the command:
    ```sh
    brew install git gnupg
    ```

3. Install the image processing libraries using brew as well:
  ```sh
  brew install imagemagick ghostscript libvips
  ```

4. Lastly, install Ruby using RVM by running the following commands:
  ```sh
  gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
  ```
  ```sh
  \curl -sSL https://get.rvm.io | bash
  ```

5. Quit and reopen the terminal. Then run the following command to get a modern Ruby that comes with Bundler:
  ``` sh
  rvm install 2.7.2
  ```

When you're done, try following along with the [Check for requirements tab](../#check-for-requirements) to make sure everything is ready to go.

## On Windows

1. First install Ruby. The [RubyInstaller for Windows 10](https://rubyinstaller.org/) is probably the easiest way to get up and running. **Make sure you install a Ruby version > 2.4 and less than 3.0!** On the last installation step make sure to run the `ridk install` step on the last step of the installation wizard.

2. Next install Git. The [Git Download page](https://git-scm.com/downloads) includes good instructions and packages for all three major operating systems.
3. Install Curl <https://curl.se/download.html>
4. Install ImageMagick by following the instructions on the [ImageMagick Downloads page](https://imagemagick.org/script/download.php#windows) **About half way down one of these is wording something like "Install legacy components (convert.exe etc)". Tick this box!**

5. Follow instructions on the [GhostScript installation page](https://docs.alfresco.com/5.0/tasks/Ghostscript-install.html).

6. Download and install [libvips](https://github.com/libvips/libvips/releases/tag/v8.11) from GitHub.

When you're done, try following along with the [Check for requirements tab](../#check-for-requirements) to make sure everything is ready to go.

## On Linux

This depends on your flavor. If you have trouble, try pinging the [Code4Lib #minicomp-wax channel](https://docs.google.com/forms/d/e/1FAIpQLSeD77mBp0Y13mFePF8UmDwFrlbxNx3VttEjz_3dgglJeK-Zbg/viewform?c=0&w=1).

When you're done, try following along with the [Check for requirements tab](../#check-for-requirements) to make sure everything is ready to go.
