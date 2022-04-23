# Vagrantbox for customized_open5gs

## Prerequisites

### Vagrant

You can install vagrant by following the steps provided here: https://www.vagrantup.com/docs/installation/

### Virtualbox

Please update the provider in the `Vagrantfile` with your favorite one.

For the Virtualbox provider you need to install virtualbox on your machine(Ubuntu). Please follow install steps here: https://www.virtualbox.org/wiki/Linux_Downloads

For mac users, look [here](https://sourabhbajaj.com/mac-setup/Vagrant/README.html)


### Vagrant additional plugins

Once vagrant is installed, you need to add this plugin. It is needed for reloading automatically the box (for kernel upgrade).

```console
$ vagrant plugin install vagrant-reload
```

## Update the box configuration

Please update the RAM and CPU values found in `Vagrantfile` to best fit you system configuration.

```console
vb.memory = <memory in KB>
vb.cpus = <number of cpus>
```
## Run it

```console
vagrant up
```

## Problem

Vagrant may not clone the repo correctly because it is a priave repo, just clone [it](https://github.com/keviniling/customized_open5gs) mannually after the vagrant box set up.
