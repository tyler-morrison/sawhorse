# Craft Sawhorse

Craft Sawhorse is a starter stack for [Craft CMS](https://craftcms.com). Based heavily upon the philosophies of [Roots Bedrock](https://roots.io/bedrock), Sawhorse is built to help you get started with development and easily deploy your Craft CMS site.

## Features

* Easy development environments with [Vagrant](http://www.vagrantup.com/)
* Dependency management with [Composer](http://getcomposer.org)
* Easy server provisioning with [Ansible](http://www.ansible.com/)
* One-command deploys

## Requirements

* PHP >= 5.5
* Composer - [Install](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)
* [Ansible](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-pip) >= 2.0.0.2
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads) >= 4.3.10
* [Vagrant](http://www.vagrantup.com/downloads.html) >= 1.5.4
* [vagrant-bindfs](https://github.com/gael-ian/vagrant-bindfs#installation) >= 0.3.1 (Windows users may skip this)
* [vagrant-hostmanager](https://github.com/smdahlen/vagrant-hostmanager#installation)


## Installation

The recommended directory structure for a Sawhorse project looks like:

```shell
example.com/            # → Root folder for the project
├── ansible/            # → Playbooks that automate server setup & deploy
├── app/                # → Craft CMS core (don’t touch!)
└── site/               # → A Craft CMS site (feel free to rename on multisite setups)
      ├── config/
      ├── plugins/
      ├── public/       # → Web root for the website
      │     ├── assets/ # → Upload folder for all Craft assets  
      │     └── dist/   # → Production ready CSS, JS, etc.
      ├── src/          # → Contains source files – Sass, uncompiled JS, etc.
      ├── storage/      # → Where Craft stores a bunch of files that get dynamically saved during use.
      ├── templates/    # → Template parts
      └── wp/   # → WordPress core (don't touch!)
```


## Deploys
