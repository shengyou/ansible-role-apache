Install Apache2 (httpd) [![Build Status](https://travis-ci.org/shengyou/ansible-role-apache.svg?branch=master)](https://travis-ci.org/shengyou/ansible-role-apache)
=========

安裝 apache2。

適用於
* Ubuntu 14.04
* Ubuntu 16.04
* CentOS 6
* CentOS 7

Requirements
------------

* ansible >= 2.4
* python >= 2.6

Role Variables
--------------

以下 Variables 非必填項目，想要設定客製的 apache2 config 才需要設置。

使用方式請參考範例。

* custom_apache2_conf
* custom_site_conf


Dependencies
------------

none.

Example Playbook
----------------

```
- name: install_apache2.yml
  hosts: myhost
  gather_facts: yes
  become: yes

  vars:
   - custom_apache2_conf: /path/to/conf/filename.conf

   - custom_site_conf::
       - src: /path/to/site_configs
         filename: site_config_filename.conf
       - src: /path/to/site_configs
         filename: site_config_filename.conf

  roles:
    - install_apache2
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
