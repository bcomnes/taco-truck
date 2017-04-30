# taco-truck

[![Greenkeeper badge](https://badges.greenkeeper.io/bcomnes/taco-truck.svg)](https://greenkeeper.io/)

Brings tacos to where you need them.

**Warning**: Highly experimental.

A tool for configuring systems, more or less [taco](https://github.com/maxogden/taco) style.  Influenced by [ansible](http://www.ansible.com/).

## Goals

- Provision and configure base images
- Unix/Node.js/Hypermodule style
- OS agnostic
- Fun
- Simple life cycle model
- Simple execution mode
- Remote execution
- Use bash scripts for simple things
- Rolls/Modules are just node modules
- Avoid as much DSLy stuff as possible. Don't reinvent the wheel.
- Try to make it possible to re-absorb configuration changes.
- Global defaults < OS Type < OS Distribution < OS Version < Roll < Host
- Apply against local host or remote host seamlessly
- Streams and pipes.  Streams and pipes.
- Simple CLI interface.
- `package.json` scripts
- infrastructure as code

## Use cases

1. [Configure OS X system](https://github.com/bcomnes/ansible-dotfiles)

2. [Configure Arch Linux system](https://github.com/bcomnes/ansible-arch-raspi)

## Initial plan

Create a system inventory.

## Imaginary CLI

```sh
$ taco-truck add # add host to the inventory
$ taco-truck remove # remove host from inventory
$ taco-truck list # list off the hosts available, (indicate which one is localhost)
$ taco-truck status # collect and display status information from providers
$ taco-truck bootstrap # Run initial setup life cycle
$ taco-truck update # run maintenance life cycle
$ taco-truck remove # run removal maintenance life cycle
```

## Motivation

System administration has a long history of doing gross, inconsistent and painful things with large numbers of computers.  Configuration management grew out of this culture and is almost equally gross.  Out of all of this grossness has emerged an entire industry dedicated putting special text files in special locations on lots of computers using snowflake DSLs, difficult to bootstrap software and big, long confusing books on how to use said DSLs correctly.

There are no configuration management systems that are written using node or the [hypermodule philosophy](http://substack.net/how_I_write_modules).  Most are written in languages with painful deployment and packaging conventions.

`taco-truck` should be used to run collections of independent modules that do something to a host system (localhost or remote via ssh).  It may offer some interfaces to make modules report consistently, or provide a writable stream that modules apply against consistently, but this will require some discovery first.


