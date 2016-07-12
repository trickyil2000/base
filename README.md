# in|ZANE Studios Base Box

Welcome to the in|ZANE studios Base Box. This is a basic LEMP stack box for development purposes, which is provisioned
with Ansible. 

## Contents
This Vagrant box contains the following packages:
 
* Ubuntu 14.04 LTS
* NGINX 1.11.2
* Redis 3.0.7
* MySQL 5.7
* ElasticSearch 2.3.3
* PHP 7.0
    * cli
    * common
    * JSON
    * opcache
    * mysql
    * phpdbg
    * mbstring
    * gd
    * imap
    * ldap
    * pgsql
    * pspell
    * recode
    * tidy
    * intl
    * curl
    * zip
    * redis
    * xdebug
    * mcrypt
* NodeJS 6.2.2
* NPM 3.10.3
* Several Common Packages
    * python-software-properties
    * build-essential
    * python-pip
    * python-dev
    * libmysqlclient-dev
    * curl
    * wget
    * unzip
    * git-core
    * ack-grep
    * htop
    * vim
    * tmux
    * software-properties-common
    * screen
    
## License
This box has been created by Rick van 't Wout Hofland (rick@in-zane.net) and has been released under Apache License, 
Version 2.0. Details about this license can be found on: https://opensource.org/licenses/Apache-2.0

## Requirements
This base box SHOULD run on ANY machine with (at least) the following specs:

* 2GB of RAM memory
* 10GB of HD space (we need plenty of space to develop in, right? ;-))
* Vagrant 1.7.2
    * Please make sure that `ffi` is installed before installing Vagrant plugins (`gem install ffi -v '1.9.14'`)  
    * Vagrant plugin 'vagrant-hostsupdater' (`vagrant plugin install vagrant-hostsupdater`)
* VirtualBox 4.3.x with extension pack
* x86 architecture

## Installation
This is the easy part :)

1. Download this repository
2. Open your terminal
3. Navigate to the folder where you've downloaded this repository
4. Type `vagrant up` (If you started up for the first time, provisioning might take a while. Please be patient!)
5. Open your browser and go to `http://www.base.dev` or `http://base.dev` and you should see a PHP status page
6. Done!

## Using the box

### General info
As stated earlier in this document, this box has been created as a "simple" box with development purposes in mind. You 
can put your application in the `/app` folder in your main folder.

### SSH
You can use the command `vagrant ssh` to enter the virtual machine.

### Starting up and powering down the box
As stated earlier, you can start up the box by using the `vagrant up` command. When you shut down your computer, it's 
recommended to use the `vagrant suspend` command to gracefully shut down your virtual machine. Alternatively, you can 
use `vagrant halt` to force your virtual machine to shut down.

### Destroying the box
When you would like to destroy your virtual machine, you can use the command `vagrant destroy`. Keep in mind that you 
have to update your `known_hosts` file in your `/.ssh/` folder, when you have used SSH to connect to your VM.

### MySQL
The box has automatically created a default database called 'base'. You can edit this database by connecting to the 
database using your favorite SQL editor (or with cli on the box itself). The default username/password combination is
`base`/`base`.

## Questions?
If you have any questions, or feature requests, you can send me an e-mail at rick@in-zane.net. Enjoy using the box!
