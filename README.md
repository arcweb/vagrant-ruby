Introduction
============

This is a template for creating a Rails 4 project hosted within a Vagrant box.

Getting Started
===============

Install the following tools before you begin:

+ VirtualBox [virtualbox.org/wiki/downloads](https://www.virtualbox.org/wiki/Downloads "virtualbox.org")
+ Vagrant [vagrantup.com/downloads.html](http://www.vagrantup.com/downloads.html "vagrantup.com")

### Start Vagrant ###

These steps only need be run once.

1. Fork this repo.
2. Clone it to a directory of your choice.
3. In your directory, run `vagrant up --provision`
4. Previous step could take some time. Grab a cup of coffee.

For most issues, you can use `vagrant provision` to re-provision the VM without restarting it.
If neccessary, use `vagrant destroy` to remove all traces of the VM and begin from scratch.

### Run ###

1. If not already running, in your vagrant directory run `vagrant up`.
2. In your vagrant directory, run `vagrant ssh` to connect to the command line of your VM.
3. Find your application in the `/vagrant` directory.
