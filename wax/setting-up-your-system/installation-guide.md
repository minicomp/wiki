---
layout: default
title: Installation guide
nav_order: 2
parent: Setting up your system
grand_parent: Wax
permalink: /wax/system-requirements/installation-guide/
---



# Installing Ruby

- **Windows 10**: The [RubyInstaller for Windows 10](https://rubyinstaller.org/) is probably the easiest way to get up and running. On the last installation step make sure to run the `ridk install` step on the last step of the installation wizard.
- **MacOS**: To install Ruby 2.4 or higher on a Mac we recommend you use Homebrew. Check on your terminal to see you if you have Homebrew installed:
    ```sh
    brew -v
    ```

    If you don't have Homebrew, visit [the Homebrew site](https://brew.sh/) for installation instructions. In the process of installing Homebrew, you may get asked to install XCode Command Line Tools. Say yes. If you succesfully install XCode, you can skip the Installing Git section below. Once Homebrew is installed you are ready to install the latest Ruby version:

    ```sh
    brew install ruby
    ```

- **Linux**: Instructions for installing Ruby on Linux can be found on the [Ruby installation site](https://www.ruby-lang.org/en/documentation/installation/).

# Installing Git

- **Windows 10 and Linux**: The [Git Download page](https://git-scm.com/downloads) includes good instructions and packages for all three major operating systems.
- **Mac**: If for some reason you still don't have git install on your Mac, the best way to do it remains to simply type `git --version` on the terminal. If you don't have it, your system will ask you to install XCode Command Line Tools. Say yes. After that process is over, git should work on your machine.

# Installing Jekyll and Bundler

- **Windows 10**: If all went well with RubyInstaller, you should be able to simply open a new command prompt window from the start menu and run: 
    ```sh
    gem install jekyll bundler
    ```
    If this doesn't work, see the [Jekyll Windows installation page](https://jekyllrb.com/docs/installation/windows/) for other options.
- **MacOS**: On your terminal run:
    ```sh
    gem install jekyll bundler
    ```
- **Linux**: To make sure that you have all the right dependencies, make sure to follow the [installation guide on the Jekyll site](https://jekyllrb.com/docs/installation/ubuntu/).

# Installing ImageMagick

[Windows](https://imagemagick.org/script/download.php#windows) and some [Unix](https://imagemagick.org/script/download.php#unix) systems come with executable installs. For Mac or other Linux flavors try the [ImageMagick installation page](http://www.besavvy.com/documentation/4-5/Editor/031350_installimgk.htm) or the [ImageMagick Downloads page](https://imagemagick.org/script/download.php).


# Installing GhostScript

Chances are you already have the GhostScript you need, but if you need the latest version the [GhostScript installation page](https://docs.alfresco.com/5.0/tasks/Ghostscript-install.html) includes good instructions and packages for all three major operating systems.
