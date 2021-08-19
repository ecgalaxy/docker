ECGALAXY docker role
====================

This Ansible role installs Docker.
It is based on geerlingguy/ansible-role-docker and supports Amazon Linux 2.

Requirements
------------

None.

Role Variables
--------------

See `defaults/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: all
      roles:
        - docker

License
-------

EUPL-1.2

Author Information
------------------

Original work: Jeff Geerling and contributors.
Modified work: ECGALAXY team.
