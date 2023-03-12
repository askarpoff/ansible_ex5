lighthouse-role
=========

Простая роль по установке lighthouse

Requirements
------------

Centos 7, Centos 8

Role Variables
--------------

| Имя           | Значение по умолчанию | Описание                        |
| -------------- | ------------- | -----------------------------------|
|lighthouse_src| https://github.com/VKCOM/lighthouse/archive/refs/heads/master.zip|ссылка на zip-архив ветки master в  git lighthouse|
|nginx_user_name|root|пользователь для запуска  nginx|

Dependencies
------------

EPEL repository for NGINX

Example Playbook
------------
```yaml
---
- name: lighthouse
  hosts: lighthouse
  roles:
    - lighthouse-role
```

License
-------

MIT

Author Information
------------------

mailto:askarpoff@gmail.com

