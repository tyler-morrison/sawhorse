# Ansible

Ansible playbooks for setting up a LEMP stack for Craft CMS.

Heavily sourced from [Roots Trellis](https://roots.io/trellis). If you have any WordPress needs, I can’t recommend the Roots team highly enough.

- Local development environment with Vagrant
- High-performance production servers
- One-command deploys

## Server Configuration

* Ubuntu 14.04 Trusty LTS
* Nginx (with optional FastCGI micro-caching)
* PHP 7.0
* MariaDB (a drop-in MySQL replacement)

## Requirements

Make sure all dependencies have been installed before moving on:

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
