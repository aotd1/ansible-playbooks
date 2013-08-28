Yii
==========

## yii

This playbook install Yii framework.
http://www.yiiframework.com/

### Vars

* **yii_version**: The Yii tag or branch (master or 1.1.14)
    * Type: String
    * Default: 1.1.14

* **yii_path**: Yii framework path
    * Type: String
    * Default: /var/www/yii

* **yii_path**: Git repository
    * Type: String
    * Default: git://github.com/yiisoft/yii.git

### Usage

``` bash
$ ansible-playbook yii.yml -uroot --extra-vars "yii_path=/var/www/yii"
```
