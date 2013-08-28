Postgresql server
======

## postgresql

These playbook install postgresql. Use it only for development, not on production (did you see pg_hba.conf? >:)

### Vars

* **postgresql_version**: Postgresql version
    * Type: String
    * Default: 9.2

* **postgresql_conf_path: Postgresql configuration file
    * Type: String
    * Default: /etc/postgresql/$postgresql_version/main

* **postgresql_unix_socket_directory: Unix socket location
    * Type: String
    * Default: /var/run/postgresql

* **postgresql_listen_port: Listen specified port
    * Type: String
    * Default: 5432

* **postgresql_listen_address: Listen interface, '*' = all.
    * Type: String
    * Default: '127.0.0.1'

* **postgresql_cluster_encoding: Postgres cluster default encoding
    * Type: String
    * Default: ru_RU.UTF-8

### Usage

``` bash
$ ansible-playbook postgresql.yml -uroot --extra-vars "postgresql_cluster_encoding=en_US"
```
