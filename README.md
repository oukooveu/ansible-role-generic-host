Ansible role: generic-host
=========

Setup "common" packages and update platform if required.

Requirements
------------

None.

Role Variables
--------------

```
ansible_run_flag: '/ansible.run'
system_force_update: false
system_packages:
  common:
    - tmux
  redhat:
    - net-tools
    - bind-utils
  debian:
    - dnsutils

```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  vars:
    system_force_update: true
  roles:
    - generic-host
```

License
-------

Apache 2.0

Author Information
------------------

Daniil Kupchenko, kupchenko@gmail.com
