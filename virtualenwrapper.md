## Installing Virtualenv and virtualenvwrapper on Ubuntu
### Follow below steps for clean setup

$ python3 --version

This should return your python version  installed

$ sudo apt-get update

$ sudo apt-get -y upgrade

$ sudo apt-get install -y python3-pip

Please note when when installing any package you will be using: sudo pip3 install thepackagename

$ sudo apt-get install build-essential libssl-dev libffi-dev python3-dev

$ sudo pip3 install virtualenv

## Confirm you have virtualenv installed

$ virtualenv --version

$ sudo pip3 install virtualenvwrapper

$ mkdir ~/.virtualenvs

$ mkdir Projects

This  directory is the /path/where/you/want/your/Projects and you can change if you like

Now Open ~/.bashrc file. This file is hidden in home and can not be easily found but you can check it by typing as below .

$  ls -la ~/ | more

Now the easy way to edit that bashrc file is using gedit or vim

$ gedit ~./bashrc

Then put the below  5 lines inside ~./bashrc preferable on top of the bashrc so that you do not mess up.
Some lazy loading here. Remember am using  $HOME/Projects here, by assuming you setup in that path.

    VIRTUALENVWRAPPER_PYTHON='/usr/bin/python3'
    export WORKON_HOME=~/.virtualenvs
    export PROJECT_HOME=$HOME/Projects
    export VIRTUALENVWRAPPER_SCRIPT=/usr/local/bin/virtualenvwrapper.sh
    source /usr/local/bin/virtualenvwrapper_lazy.sh

After putting these just save the ~./bashrc and please **DO NOT** screw this file.
Now still on command line continue as below. You must source that bashrc

$ source ~./bashrc

## Congratulations you are now done!

### The neat way to create a virtual env can now be done as below

$ mkproject my_project

$ workon my_project

Youll see something like (my_project) proving you have activated the virtual  environment.  You must see those parenthesis .


To deactivate and get out of the env
$ deactivate

### Always ensure you activate when installing things like Django.. otherwise versions will mess you up

# I hope this helps 
