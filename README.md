mariadb
=========

[![Build Status](https://travis-ci.org/kilerkarol/mariadb.svg?branch=master)](https://travis-ci.org/kilerkarol/mariadb)

Role install and configure mariadb.

Role Variables
--------------

Default variables for that role
```
    mariadb_purge: false
```

Variable set to get default ansible variable form inventory `ansible_port` 
```
    ssh_port: "{{ ansible_port }}"
```

Other variables for that role:
```
    mariadb_version: "10.0.31"

    mariadb_packages:
        - { name: "mariadb-server", version: "{{ mariadb_version }}", state: "present" }
        - { name: "mariadb-client", version: "{{ mariadb_version }}", state: "present" }
```    

Example Playbook
----------------

```
  - hosts: servers
    roles:
      - { role: kilerkarol.mariadb, tag: mariadb }
```

License
-------

BSD

Author Information
------------------

Karol Kieglerski