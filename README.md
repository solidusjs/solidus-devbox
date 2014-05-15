# Solidus Development Environment

This repo is designed to help you easily get Solidus sites running locally for development. We accomplish this largely by running everything within a Linux virtual machine. It’s easy to get up and running, time required is primarily to download everything. This repo contains a basic [Vagrantfile][vagrantfile], configured to use the [vagrant-solidus][vagrant-solidus] plugin. The plugin handles everything necessary to run your Solidus sites.

## [Install VirtualBox][virtualbox-install]

[VirtualBox][virtualbox] is a free cross-platform virtualization app that makes it easy to simultaneously run multiple operating systems on your machine. In our usage it is merely a [provider][vagrant-provider] for Vagrant.

## [Install Vagrant][vagrant-install]

[Vagrant][vagrant] layers provisioning, file-based configuration, and a command-line interface on top of VirtualBox. This provides disposable, consistent environments for running development servers. [Synced Folders][vagrant-synced-folders] and [Networking][vagrant-networking] features make the development experience the same as if running in your own environment: your own tools and whatever ports you’d like for access via your browser and other clients.

## Install vagrant-solidus

This [Vagrant plugin][vagrant-solidus] will let you manage your Solidus sites through the command line.

```
$ vagrant plugin install vagrant-solidus
```

## Up!

You are now ready to clone this repo and start the virtual machine:

```
$ git clone https://github.com/solidusjs/solidus-devbox.git
$ cd solidus-devbox
$ vagrant up
```

This will boot the VM, and automatically install and configure everything that is required to run Solidus sites, a process called [Provisioning][vagrant-provisioning]: `Vagrantfile` defines a pre-built 64-bit Ubuntu 12.04.3 LTS (Precise) “box” provided by the Vagrant team. This file also defines basic configuration such as port mapping and synced folder locations, it can be updated at any time. New boxes are only downloaded to your machine the first time you provision a new VM however. Once the operating system is booted, this plugin will perform additional provisioning. You can redo the provisioning process at any time by running `vagrant provision`.

At this point, you are ready to work on your Solidus site! Take a look at the vagrant-solidus [documentation][vagrant-solidus] to continue.


[vagrant]: http://www.vagrantup.com
[vagrantfile]: https://docs.vagrantup.com/v2/vagrantfile/
[vagrant-provider]: http://docs.vagrantup.com/v2/providers
[vagrant-install]: http://www.vagrantup.com/downloads.html
[vagrant-synced-folders]: http://docs.vagrantup.com/v2/synced-folders/index.html
[vagrant-networking]: http://docs.vagrantup.com/v2/networking/index.html
[vagrant-provisioning]: http://docs.vagrantup.com/v2/provisioning/index.html
[vagrant-solidus]: https://github.com/solidusjs/vagrant-solidus
[virtualbox]: https://www.virtualbox.org
[virtualbox-install]: https://www.virtualbox.org/wiki/Downloads
