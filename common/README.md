User space
==========

## user-space

Install mc, vim and htop utilities =)

### Usage

``` bash
$ ansible-playbook user-space.yml -uroot
```

## upgrade

sudo apt-get update && sudo apt-get dist-upgrade

### Usage

``` bash
$ ansible-playbook upgrade.yml -uroot
```

## locale

Add specified locale in system.
Based on https://github.com/kalos/playbook-debian_base/

### Vars

* **lang**: locale language
    * Type: String
    * Default: ru_RU

### Usage

``` bash
$ ansible-playbook locale.yml -uroot --extra-vars "lang=ru_RU"
```

## timezone

Add specified locale in system.
Based on https://github.com/kalos/playbook-debian_base/

### Vars

* **timezone**: Timezone
    * Type: String
    * Default: Asia/Novosibirsk

### Usage

``` bash
$ ansible-playbook locale.yml -uroot --extra-vars "timezone=Europe/Moscow"
```
