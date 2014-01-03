# My Personal Vagrant Setup

A basic Ubuntu 12.04 Vagrant setup with PHP 5.5 and MySQL 5.5.
PHP 5.4 w/ Apache 2.2 is available on the php54 branch.

## Requirements

* VirtualBox - Free virtualization software [Download Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* Vagrant **1.3+** - Tool for working with virtualbox images [Download Vagrant](https://www.vagrantup.com)
* Git - Source Control Management [Download Git](http://git-scm.com/downloads)

## Setup

* Clone this repository `git clone https://github.com/pedrommone/my-vagrant-setup.git`
* (you can change the database settings inside the vagrant-install.sh file)
* run `vagrant up` inside the newly created directory
* (the first time you run vagrant it will need to fetch the virtual box image which is ~300mb so depending on your download speed this could take some time)
* You can verify that everything was successful by opening http://localhost in a browser

*Note: You may have to change permissions on the www/app/storage folder to 777 under the host OS* 

For example: `chmod -R 777 www/app/storage/`

## Usage

Some basic information on interacting with the vagrant box

### Port Forwards

* 80 - Apache

### Default MySQL Database

* User: vagrant
* Password: vagrant
* DB Name: vagrant

### Vagrant

Vagrant is [very well documented](http://vagrantup.com/v1/docs/index.html) but here are a few common commands:

* `vagrant up` starts the virtual machine and provisions it
* `vagrant suspend` will essentially put the machine to 'sleep' with `vagrant resume` waking it back up
* `vagrant halt` attempts a graceful shutdown of the machine and will need to be brought back with `vagrant up`
* `vagrant ssh` gives you shell access to the virtual machine

### Virtual Machine Specifications

* OS     - Ubuntu 12.04
* Apache - 2.4.6
* PHP    - 5.5.4
* MySQL  - 5.5.3

## Thanks to

* @andrew13
* @bryannielsen
* @JeffreyWay