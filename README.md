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

One-liner
---------

    bash <(curl -s https://code.europa.eu/-/snippets/1/raw/main/ansible-role.sh) ecgalaxy.docker

See [ansible-role](https://code.europa.eu/-/snippets/1) for instructions.

Please verify the script integrity first.

Upgrading & Uninstalling
------------------------

This Ansible role uses the distribution's package manager to install packages.

In order to upgrade or uninstall a package, please refer to your distribution's package manager documentation.

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
