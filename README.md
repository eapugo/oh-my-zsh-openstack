# oh-my-zsh Openstack client tools completion plugin

This is a plugin auto completing openstack client tools. It's based on https://github.com/rbirnie/oh-my-zsh-nova.

It autocompletes nova/glance subcommands, and it also knows about available resources - instances, images, security groups.

## Installation

In order to take advantage of this, you have to install:

* Particular client tools: python-{nova,glance,neutron}-client.
* The cache building script ([build\_cache.py|https://github.com/t0mk/openstack-utils/blob/master/build\_cache.py]) from https://github.com/t0mk/openstack-utils as cronjob. It builds the cache so list of resources is available offline.

Installation of this repo:

```
$ cd
$ git clone https://github.com/t0mk/oh-my-zsh-openstack
# Following creates symlinks to this repo in you custom/ space in .oh-my-zsh
# Works best if you cloned repo to your home dir. Run this from home dir too.
$ for d in $(find `pwd`/oh-my-zsh-openstack -mindepth 1 -maxdepth 1 -type d -not -iwholename '*.git'); do echo `basename $d`; ln -s $d .oh-my-zsh/custom/plugins/`basename $d`; done
```

And then add printed plugin names to the plugins array in your .zshrc.

