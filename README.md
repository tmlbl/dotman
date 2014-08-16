dotman
======

A simple bash script for managing dotfiles.

### The Problem
I have configuration files in different locations on my machine, and I want to keep up-to-date copies of them together in a git repository, while keeping them in their existing locations as well.

### Installation
Just copy the script into your bin:

`sudo cp dotman /usr/bin/dotman`

### Usage
Add a file to the register:

`dotman add vim ~/.vimrc`

This command will create a .dotman file in the current directory and add your .vimrc file path to it. Now anytime you want to import the latest version of your .vimrc file, just execute:

`dotman import vim`

And you're done!

