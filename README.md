ECGALAXY docker role
====================

This Ansible role installs Docker.

It is based on [ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker) and supports Amazon Linux 2.

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
        - ecgalaxy.docker

License
-------

Copyright the European Union 2022.

Licensed under the EUPL-1.2 or later.

Original work
-------------

Copyright Jeff Geerling.

See https://github.com/geerlingguy/ansible-role-docker

Author Information
------------------

Original work: Jeff Geerling and contributors.

Modified work: ECGALAXY team.
