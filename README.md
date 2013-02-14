# Vagrant Rails App Starter

---

A Ruby on Rails project starter, utilizing a Vagrant VM (default: Ubuntu Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [nodejs](https://github.com/mdxp/nodejs-cookbook.git)
* [rvm](https://github.com/fnichol/chef-rvm)
* [vim](https://github.com/opscode-cookbooks/vim)

## Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Librarian](https://github.com/applicationsonline/librarian)

## Usage

Clone it into your project folder, install cookbook dependencies with Librarian-Chef, launch/create Vagrant VM...

    > git clone https://github.com/devert/vagrant-rails-app-starter [project-name]
    > rm -rf .git

Open the vagrant/Vagrantfile and modify *proj-name* instances to the name of your project. Modify the Node.js and Ruby versions you would like installed in the *chef.json* attributes. Additionally, list any additional gems you would like installed in the *global_gems* array. See [chef_rvm](https://github.com/fnichol/chef-rvm) documentation for more details on rvm configuration.

Type these commands on the terminal

    cd vagrant
    librarian-chef install
    vagrant up
    vagrant reload
    vagrant ssh
    cd proj-name
    sudo gem install rails
    rails new .
        Overwrite /home/vagrant/proj-name/.gitignore? (enter "h" for help) [Ynaqdh] y
    rails server

After running the above commands you should be able to browse to http://locahost:3000/ and see the rails "Welcome aboard" page. Changes to files via the host machine will immediately be updated on the guest VM as well. Now get in there and build something awesometronic with Ruby on Rails!

## Optional (But Pretty Great)

#### Vagrant
* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin. Install this on the host machine.
		
		> vagrant gem install vagrant-vbguest

* Setup a custom host name for Vagrant VM and host OS with [vagrant-hostmaster](https://github.com/mosaicxm/vagrant-hostmaster.git). Install this on the host machine.
	
		> vagrant gem install vagrant-hostmaster

	```ruby
	# Uncomment the following in Vagrantfile
	config.hosts.name = "proj-name.local"
	```




