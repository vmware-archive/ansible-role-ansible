# ansible-role-ansible

Ansible playbook to automate upgrading Ansible and necessary libraries for SuperVIO.

## Requirements

This role currently supports only Debian/Ubuntu distros.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    update_package_cache: True

Whether to update the aptitude, yum, pacman or other package cache before running any install tasks.

    ansible_services:
      - lxdm

The services (that should get installed and loaded in addition to basic Ansible needs.
For instance, lxdm will install and set enable the Lightweight X Desktop Manager for
login and general window services on a development machine.

## Example playbook

```
---
- hosts: supervio
  sudo: True
  connection: local
  roles:
    - ansible
    - repo
  vars:
    - aptitude_update: False
```

## License

TBD

## Author Information

This role was created in 2015 by [Tom Hite / VMware](http://www.vmware.com/).
