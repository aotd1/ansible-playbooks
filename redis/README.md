Redis server
==========

## redis

This playbook install and configure redis server

### Vars

* **swappiness**: The swappiness value (range 0 to 100)
    * Type: Integer
    * Default: 60

* **redis_dest_config**: Redis config path
    * Type: String
    * Default: /etc/redis/redis.conf

* **redis_port**: Listen on specified port. If port is set to 0 redis will not listen on a TCP socket.
    * Type: Integer
    * Default: 6379

* **redis_interface**: Listen interface
    * Type: String
    * Default: 0.0.0.0

* **redis_unix_socket**: Unix socket
    * Type: String
    * Default: /var/run/redis/redis.sock

* **redis_unix_socket_permissions**: Unix socket permissions
    * Type: Integer
    * Default: 777

* **redis_log_level**: Log level
    * Type: String
    * Default: notice

* **redis_databases**: Databases count
    * Type: Integer
    * Default: 16

* **redis_ram_only**: Store data in RAM memory only, don't flush on disk
    * Type: Boolean
    * Default: true

* **redis_timeout**: Connection timeout
    * Type: Integer
    * Default: 100

* **redis_maxmemory.limit**: Maximum memory limit
    * Type: String
    * Default: 3gb

* **redis_maxmemory.policy**: Memory flush policy
    * Type: String
    * Default: volatile-lru

### Usage

``` bash
$ ansible-playbook redis.yml -uroot --extra-vars "redis_databases=2"
```

## redis-remove

This playbook removes redis server

### Usage

``` bash
$ ansible-playbook redis-remove.yml -uroot
```