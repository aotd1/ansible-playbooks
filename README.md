ansible-playbooks
=================

A simple and quick way to deploy development environment.

Tested on:
 - Ubuntu 10.04 x32/64 (broken postgresql and php5-fpm pool)
 - Ubuntu 12.04 x32/64 - recommend
 - Ubuntu 13.04 x32/64
 - Debian 7.0 x32/x64 (broken postgresql)

`environment.yml` installs vim, mc, htop, git, php5-fpm, nginx, mysql.
Setups nginx<-->php-fpm upstream php-local and tune configuration files.

`environment-full-test.yml` included to test all playbooks.

## Usage

Edit `environment.yml` and set specified variables. Copy `hosts.example` to `hosts` and add VM IPs.
````
ansible-playbook -uroot -k -ihosts environment.yml
````