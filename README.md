# Ansible Role: EPEL Repository

[![Build Status](https://travis-ci.org/chauanhtuandl/ansible-role.mongodb.svg?branch=master)](https://travis-ci.org/chauanhtuandl/ansible-role.mongodb)

Installs the [MongoDB](https://www.mongodb.com/) for RHEL/CentOS/Debian/Ubuntu.

## Requirements

This role require pymongo library.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    packages_name: The name of the package MongoDB org.
    service_name: The name of the service MongoDB on the OS.
    service_service_state: This is state flag to start, stop, restart, reload service. You can see more detail at [state](https://docs.ansible.com/ansible/latest/modules/service_module.html#parameter-state). Default: start
    service_service_enabled: Whether the service should start on boot.
    mongo_access_control_enabled: This is conditional to trigger create authentication on MongoDB.
    mongodb_user_ac: The name of the user will be create when mongo_access_control_enabled is true
    mongodb_user_roles: The role of the user will be add when mongo_access_control_enabled is true

## Dependencies

This role require the role [chauanhtuan.pip](https://github.com/chauanhtuandl/ansible-role.pip) to install pymongo library.

## Example Playbook

    - hosts: servers
      roles:
        - chauanhtuandl.pip
        - chauanhtuandl.mongodb

## License

MIT / BSD

## Author Information

This role was created/edited in 2020 by Chau Anh Tuan.
