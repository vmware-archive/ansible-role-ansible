# ansible-role-ansible

Ansible playbook to automate upgrading Ansible and necessary libraries for SuperVIO.

## Requirements

This role currently supports only Debian/Ubuntu distros.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    update_package_cache: True

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
