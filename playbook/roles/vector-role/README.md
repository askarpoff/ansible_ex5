vector-role
=========

Простоя роль по установке Vector

Requirements
------------
Centos 7, Centos 8


Role Variables
--------------

| Имя           | Значение по умолчанию | Описание                        |
| -------------- | ------------- | -----------------------------------|
| vector_version | "0.27.0" | Версия Vector |

Dependencies
------------

No depedencies



Example Playbook
------------
```yaml
---
- name: vector
  hosts: vector
  roles:
    - vector-role
```



License
-------

MIT

Author Information
------------------

mailto:askarpoff@gmail.com


