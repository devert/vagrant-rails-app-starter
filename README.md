# Vagrant Rails App Starter

A Ruby on Rails project starter, utilizing a Vagrant VM (default: Ubuntu 12.04 Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [nodejs](https://github.com/mdxp/nodejs-cookbook)
* [rbenv](https://github.com/fnichol/chef-rbenv)
* [ruby_build](https://github.com/fnichol/chef-ruby_build)
* [vim](https://github.com/opscode-cookbooks/vim)

## Dependencies

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Vagrant Librarian-Chef](https://github.com/jimmycuadra/vagrant-librarian-chef)

## Usage

Clone it into your project folder.

```bash
$ git clone https://github.com/devert/vagrant-rails-app-starter [project-name]
$ rm -rf .git
```

Open the vagrant/Vagrantfile and modify *proj-name* instances to the name of your project. Modify the Node.js and Ruby versions you would like installed in the *chef.json* attributes. Additionally, list any additional gems you would like installed in the *gems* array. See [chef-rbenv](https://github.com/fnichol/chef-rbenv) documentation for more details on rbenv configuration.

```bash
$ vagrant plugin install vagrant-librarian-chef
$ cd vagrant
$ vagrant up
$ vagrant ssh
$ cd proj-name
$ sudo rails new .
Overwrite /home/vagrant/proj-name/.gitignore? (enter "h" for help) [Ynaqdh] y
$ rails server
```

If the above fails when running the `sudo rails new .` command, try running `sudo bundle install` and then run `rails new .` again.

After running the above commands you should be able to browse to http://locahost:3000/ and see the rails "Welcome aboard" page. Changes to files via the host machine will immediately be updated on the guest VM as well. 

Now get in there and build something awesometronic with Ruby on Rails!

## Optional (But Pretty Great)

#### Vagrant
* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin. Install this on the host machine.

    ```bash
    $ vagrant gem install vagrant-vbguest
    ```




