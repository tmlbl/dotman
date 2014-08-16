dotman
======

A simple bash script for managing dotfile repositories.

### Installation
Clone this repository, then copy the script into your bin:

`sudo cp dotman /usr/bin/dotman`

Or, if you prefer one easy step:

`sudo curl -o /usr/bin/dotman https://raw.githubusercontent.com/tmlbl/dotman/master/dotman && sudo chmod +x /usr/bin/dotman`

### Usage

#### Creating a dotfiles repository
I usually create a .dotfiles directory in my HOME folder:

````
mkdir ~/.dotfiles
cd ~/.dotfiles
git init
git remote add origin <git_url>
````
Then, start adding config files with dotman:
````
dotman add ~/.vimrc vimrc
dotman add ~/.config/sublime-text-3/Packages/User/Preferences.sublime-settings subl
````
When you make changes to a config and want to add them to your dotfiles repo:
````
cd ~/.dotfiles
dotman import subl
````
Then, use git normally to version your files. If you pull changes from git that you want to use on your machine, just:
`dotman export subl`
And the changes will be written to the destination path.
