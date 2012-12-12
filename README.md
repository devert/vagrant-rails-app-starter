# Vagrant Ruby App Starter

### Intro

A Ruby project starter, utilizing a Vagrant VM (default: Ubuntu Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [vim](https://github.com/opscode-cookbooks/vim)

### Requirements

* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Librarian](https://github.com/applicationsonline/librarian)

### Usage

Clone it into your project folder, install cookbook dependencies with Librarian-Chef, launch/create Vagrant VM...

    git clone https://github.com/devert/vagrant-ruby-app-starter project-name
    rm -rf .git
    cd vagrant
    librarian-chef install
    vagrant up
    vagrant ssh
    cd project-name


