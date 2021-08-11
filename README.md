ECGALAXY docker
=======================

This role installs Docker and docker-compose.

Requirements
------------

None.

Role Variables
--------------

- `docker_edition`: 'ce' Edition can be one of: 'ce' (Community Edition) or 'ee' (Enterprise Edition).
- `docker_package`: "docker-{{ docker_edition }}"
- `docker_package_state`: present

Service options.
- `docker_service_state`: started
- `docker_service_enabled`: true
- `docker_restart_handler_state`: restarted

Docker Compose options.
- `docker_install_compose`: true
- `docker_compose_version`: "1.26.0"
- `docker_compose_url`: https://github.com/docker/compose/releases/download/{{ docker_compose_version }}/docker-compose-Linux-x86_64
- `docker_compose_path`: /usr/local/bin/docker-compose

Used only for Debian/Ubuntu. Switch 'stable' to 'nightly' if needed.
- `docker_repo_url`: https://download.docker.com/linux
- `docker_apt_release_channel`: stable
- `docker_apt_arch`: amd64
- `docker_apt_repository`: "deb [arch={{ docker_apt_arch }}] {{ docker_repo_url }}/{{ ansible_distribution | lower }} {{ ansible_distribution_release }} {{ docker_apt_release_channel }}"
- `docker_apt_ignore_key_error`: true
- `docker_apt_gpg_key`: "{{ docker_repo_url }}/{{ ansible_distribution | lower }}/gpg"

Used only for RedHat/CentOS/Fedora.
- `docker_yum_repo_url`: "{{ docker_repo_url }}/{{ (ansible_distribution == 'Fedora') | ternary('fedora','centos') }}/docker-{{ docker_edition }}.repo"
- `docker_yum_repo_enable_nightly`: '0'
- `docker_yum_repo_enable_test`: '0'
- `docker_yum_gpg_key`: "{{ docker_repo_url }}/centos/gpg"

A list of users who will be added to the docker group.
- `docker_users`: []

Docker daemon options as a dict
- `docker_daemon_options`: {}

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

ECGALAXY team.
