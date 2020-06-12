Role Name
=========

This role will transfer a routeros image file to a mikrotik device, and then reboot the device for installation.

Requirements
------------

NA

Role Variables
--------------

Timeout is currently set to 2 minutes in the variable file.

Dependencies
------------

NA

Example Playbook
----------------

```
---
- name: Check ROS and upgrade if needed
  hosts: mtk1
  gather_facts: no
  strategy: free
  vars:
# I recommend setting the timeout to two minutes or even longer depending on how long it takes the device to pull the file.
    ansible_command_timeout: 120

  roles:
    - mtk-ros-upgrade-file
```

License
-------

BSD

Author Information
------------------

Greg Sowell 2020 - GregSowell.com / TheBrothersWISP.com
