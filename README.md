# Vagrant Rails App Starter

### Intro

***WORK IN PROGRESS.*** *Currently not functional.*

A Rails 3 project starter, utilizing a Vagrant VM (default: Ubuntu Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [vim](https://github.com/opscode-cookbooks/vim)

### Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Librarian](https://github.com/applicationsonline/librarian)

## Optional

* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin.

### Usage

Clone it into your project folder, install cookbook dependencies with Librarian-Chef, launch/create Vagrant VM...

    $ git clone https://github.com/devert/vagrant-rails-app-starter project-name
    $ rm -rf .git
    $ cd vagrant
    $ librarian-chef install
    $ vagrant up
    $ vagrant ssh
    $ cd project-name


