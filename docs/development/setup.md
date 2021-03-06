Setup
=====

Variables used in templates:

* `{{BASE_URL}}`: Base url including protocol, domain name and base path. Does not end with `/`. E.g. `https://www.example.com`.
* `{{SITENAME}}`: Title of your project.
* `{{PAGE_RELATIVE_URL}}`: URL of current document relative to base path. Does start with a `/`. E.g. `/example/index.html`.
* `{{PAGE_TITLE}}`: Title of the current page.
* `{{PAGE_DESCRIPTION}}`: Description of the current page. Maximum length is 160 characters.
* `{{THEME_COLOR}}`: Hex color used as basic theme color. E.g. `#aa00ff`.

There are also some variables used for automatic setups (see [setup.sh](../../build/setup.sh):

* `{{DB_TABLE}}`
* `{{DB_USERNAME}}`
* `{{DB_PASSWORD}}`

Using the setup script
----------------------

If you want to use automatic setups via [setup.sh](../../build/setup.sh), you may have to modify if extensively.

Web server in a box
--------------------

You may want to use [Vagrant](https://www.vagrantup.com/). This will offer you an easy setup for virtual machines.

For virtualisation to work you will need a VM client. You may want to use:

* [Virtual Box](https://www.virtualbox.org/)

This project comes pre-equipped with [Scotch Box](https://box.scotch.io/). For more complex setups consider using [PuPHPet](https://puphpet.com/).

The most important commands:

* `vagrant up`: Start/resume your server.
* `vagrant suspend`: Pause your server. You should do this before shutting down your computer.
* `vagrant halt`: Shutdown your server.
* `vagrant destroy`: Delete your server. This will keep all data in your local directory, and allows for a clean re-installation.
* `vagrant ssh`: SSH into your server.
* `vagrant provision`: Run provisioner again.

Additonal commands:

* `vagrant box update`: Run update of OS.
* `vagrant plugin install vagrant-vbguest`: Install guest plugin for Virtual Box.

The local Vagrant setup will execute any commands from [`build/vagrant/bootstrap.sh`](../../build/vagrant/bootstrap.sh). In this case Vagrant will install all required dependencies for your project and start the [Gulp watcher](gulp.md).

After starting Vagrant there will be a webserver, running at the host name you set it to under [`build/vagrant/Vagrantfile`](../../build/vagrant/Vagrantfile).

