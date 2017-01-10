traefik
=========

[![Build Status](https://travis-ci.org/jebovic/ansible-traefik.svg?branch=master)](https://travis-ci.org/jebovic/ansible-traefik) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.traefik-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/traefik)

Install and configure traefik

This role is a part of my [OPS project](https://github.com/jebovic/ops), follow this link to see it in action. OPS provides a lot of stuff, like a vagrant file for development VMs, playbooks for roles orchestration, inventory files, examples for roles configuration, ansible configuration file, and many more.

Dependencies
------------

This role depends on [jebovic.supervisor](https://github.com/jebovic/ansible-supervisor) role to be fully functional

Role Variables
--------------

```yaml
# Traefik installation configuration
traefik_install_dir: /usr/local/bin
traefik_binary_url: https://github.com/containous/traefik/releases/download/v1.1.2/traefik_linux-amd64
traefik_bin_path: "{{ traefik_install_dir }}/traefik"
traefik_config_dir: /etc/traefik

traefik_static_config: |
                        # Add your custom static config here

traefik_dynamic_config: |
                        # Add your custom dynamic config here
```

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
     - { role: jebovic.traefik }
```

Tags
----

* traefik_config : only update config and restart service


License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic
