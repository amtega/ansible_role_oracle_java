# Amtega oracle_java role

This is an [Ansible](http://www.ansible.com) role to deploy Oracle Java.

## Requirements

[Ansible 2.6+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

The role setups the following facts:

- oracle_java_home: home path of the deployed oracle java

## Dependencies

[amtega.artifact](https://galaxy.ansible.com/amtega/artifact)

## Example Playbook

This is an example playbook:

``` yaml
---
- name: oracle java role sample
  hosts: localhost
  roles:  
    - amtega.oracle_java
  vars:
    oracle_java_state: present
    oracle_java_version: latest
    oracle_java_accept_license: true
    oracle_java_remove_artifact: false
```

## Testing

Tests are based on docker containers. You can setup docker engine quickly using the playbook `files/setup.yml` available in the role [amtega.docker_engine](https://galaxy.ansible.com/amtega/docker_engine).

Once you have docker, you can run the tests with the following commands:

```shell
$ cd amtega.oracle_java/tests
$ ansible-playbook main.yml
```

## License

Copyright (C) 2018 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.
