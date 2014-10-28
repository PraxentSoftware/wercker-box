# Astonish Design Standard Wercker Box
[![wercker status](https://app.wercker.com/status/da62deaa330891af10ea369d2ce48339/m/ "wercker status")](https://app.wercker.com/project/bykey/da62deaa330891af10ea369d2ce48339)

Provisioned with Ansible

Includes:
- nodejs
- grunt-cli
- ruby
- bundler
- php54
- composer
- phpunit
- mongoDB
- phantomjs

## To test and build locally, use [Vagrant](https://www.vagrantup.com/):

### Set up the test box
  - cd into a sandbox directory `mkdir ../sandbox; cd ../sandbox`
  - Create a new vagrant repository with `vagrant init`
  - Copy provision.yml `cp ../wercker-box provision.yml .`
  - edit 'hosts' on line two to be 'all':
```---
   - hosts: all
     remote_user: vagrant
```
  - Run `vagrant up`

### Make changes and have them applied
  - Make changes to the provision.yml file
  - Run `vagrant provision`
  - Check out the box with `vagrant ssh`
