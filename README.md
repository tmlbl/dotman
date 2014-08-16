dotman
======

A simple bash script for managing dotfile repositories.

### The Problem
I have configuration files in different locations on my machine, and I want to keep up-to-date copies of them together in a git repository, while keeping them in their existing locations as well.

### Installation
Clone this repository, then copy the script into your bin:

`sudo cp dotman /usr/bin/dotman`

Or, if you prefer one easy step:

`sudo curl -o /usr/bin/dotman https://raw.githubusercontent.com/tmlbl/dotman/master/dotman && sudo chmod +x /usr/bin/dotman`

### Usage
Add a file to the register:

`dotman add vim ~/.vimrc`

This command will create a .dotman file in the current directory and add your .vimrc file path to it. Now anytime you want to import the latest version of your .vimrc file, just execute:

`dotman import vim`

And you're done!

