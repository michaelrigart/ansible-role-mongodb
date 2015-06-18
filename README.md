Ansible mongodb Role
====================
[![Build Status](https://semaphoreci.com/api/v1/projects/934de807-f52f-48f2-a11a-e601510fc287/459467/badge.svg)](https://semaphoreci.com/michaelrigart/ansible-role-mongodb) [![Build Status](https://travis-ci.org/michaelrigart/ansible-role-mongodb.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-mongodb)

An ansible role for installing and configuring mongodb

Role Variables
--------------

```yaml
mongodb_pymongo_ppa_repo: 
mongodb_pkg_version:
mongodb_pkg_state: installed
mongodb_admin_user: dict holding the "admin" user you want to create
  username: admin username
  database: database to add user to (most likely admin)
  password: admin password
  roles: roles you want to assign to the admin user
  state: the state of the admin user (most likely present)
mongodb_conf: dict holding the key / values of your configuration
mongodb_logrotate_options: list with the logrotate options
mongodb_service_state: indicates the service state; Allowed setting: started, stopped
mongodb_service_enabled: indicates if service needs to be enabled on boot; Allowed settings: yes, no
```

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.mongodb, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>