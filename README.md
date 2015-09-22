Developer setup for any new Mac
---

It's hard to remember which tools you have installed on the other machine to develop web pages. This guide helps you to setup your new Mac.

First of install, be sure to install [Xcode](https://itunes.apple.com/de/app/xcode/id497799835?mt=12) from Mac AppStore, to get [git](https://git-scm.com/). Start it once to accept the terms of use.

## Installation

```sh
# Homebrew (Package Tool for Mac Apps)
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Android Debug Bridge (adb) to
# communicate with Android Devices
$ brew install android-platform-tools
```

### git

Install [git](https://git-scm.com/download/mac) directly or via [Xcode](https://itunes.apple.com/de/app/xcode/id497799835?mt=12). Start Xcode one to acccept the terms of use. Check, if git is installed properly by typing `git --version`.

#### SSH Public key

Copy your private key to your computer and set permissions.

```sh
$ cd /Volumes/<your-usb-stick>/.ssh
$ cp config macx macx.pub ~/.ssh
$ chmod 700 ~/.ssh && chmod 600 ~/.ssh/macx && chmod 644 macx.pub
$ ssh-add ~/.ssh/macx
```

### Setup a proper Terminal

I'm using [TotalTerminal](http://totalterminal.binaryage.com/) to slide up the terminal from the bottom of any screen. But the most important thing is to use proper [Dotfiles](http://dotfiles.github.io/). My favourite set is from [Mathias Bynens](https://github.com/mathiasbynens/dotfiles).

```sh
# Clone the Repository and modify it to fit your needs
$ git clone https://github.com/mathiasbynens/dotfiles.git && cd dotfiles && source bootstrap.sh

# Copy the new Dotfiles to your user folder
$ source bootstrap.sh
```

## Editors

### Sublime Text

Download [Sublime Text 3](http://www.sublimetext.com/3) and install it.

Now, let's use `subl` as a command to start it from the command line:

```sh
$ mkdir ~/bin
$ ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl
```

## Install Build tools

```sh
$ npm install -g babel     # Babel JavaScript Compiler
$ gem install scss_lint    # Sass-Linter
```
