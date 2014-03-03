# kitchen-vagrant-metal

VagrantMetal - a driver for Test Kitchen that wraps around Metal's Vagrant driver.

This is a gem that uses Metal to execute a driver that Test Kitchen can use.
I.e., install this gem (and Metal and maybe the Metal Vagrant driver if it ever gets
split out and dependencies as needed) and use it as the vagrant_metal driver.

## Requirements

Requires Chef Metal and Test Kitchen.

## Installation

Installation is fairly easy, simply run the following commands in the main directory here:

```
gem build kitchen-vagrant-metal.gemspec
gem install ./kitchen-vagrant-metal-0.1.0.dev.gem 
```

## Notes

This gem is experimental and a bit touchy; it has only shaky support for multiple OS
types and running multiple operations back-to-back (i.e., sometimes it will choke
for no good reason doing something like 'kitchen verify' on a converged box if you
don't do the 'kitchen setup' separately first).

Given that this is basically a proof-of-concept, we don't plan to do much more in
terms of development or support, so, you know, don't use this in production or
anything.  Obviously.

## Authors

Created mainly by Douglas Triggs <doug@getchef.com> with help from John Keiser
<jkeiser@getchef.com> based on the structure of the kitchen-vagrant driver written
by Fletcher Nichol <fnichol@nichol.ca>.
