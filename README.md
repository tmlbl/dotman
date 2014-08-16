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
Or, make changes to the file inside your .dotfiles directory:
````
cd ~/.dotfiles
subl subl # make some changes
dotman export subl
````
#### Importing a dotfiles repository
Clone the dotfiles repository and cd into it, ie:
````
git clone git@github.com:tmlbl/crunchbookpro
cd crunchbookpro
````
Then, if you want to use the "vimrc" file, do:
````
dotman add ~/.vimrc vimrc
dotman export vimrc
````
### Development

#### Running the tests
The tests require you have docker up and running, and are able to run docker without sudo. To verify this:
````
docker ps
````
To run the tests:
````
./test/run
````
dotman is tested on Ubuntu, Centos and SUSE using docker.

#### Workflow
As soon as the dotman file is edited you may test your changes by using that executable, ie:
````
./dotman ls
````
