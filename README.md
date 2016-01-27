[![Build Status](https://travis-ci.org/code-n-beer/ansible-docker.svg?branch=master)](https://travis-ci.org/code-n-beer/ansible-docker)

Ansible Docker
=========

This role is for installing Docker.

Requirements
------------

Ansible 2.0

For testing with Vagrant:

Virtualbox 5.0+
Vagrant 1.7.4+

Role Variables
--------------
In development.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
         - code-n-beer.ansible-docker

Testing
--------

Run `vagrant up`. To see what it does, read `Vagrantfile` and `tests/vagrant.yml`.

License
-------

BSD

Author Information
------------------

CNB Ltd.
