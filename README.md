# ansible_ex5

### Molecule

1. Запустите  `molecule test -s centos_7` внутри корневой директории clickhouse-role, посмотрите на вывод команды. Данная команда может отработать с ошибками, это нормально. Наша цель - посмотреть как другие в реальном мире используют молекулу.
<details>
  <summary>molecule test -s centos_7</summary>
  
```bash 
debian@debian:~/ansible_ex5/playbook/roles/clickhouse$ molecule test -s centos_7
INFO     centos_7 scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/230ee0/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/230ee0/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/230ee0/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > lint
COMMAND: yamllint .
ansible-lint
flake8

/bin/bash: yamllint: command not found
Usage: ansible-lint [options] playbook.yml [playbook2 ...]

Options:
  --version             show program's version number and exit
  -h, --help            show this help message and exit
  -L                    list all the rules
  -q                    quieter, although not silent output
  -p                    parseable output in the format of pep8
  --parseable-severity  parseable output including severity of rule
  -r RULESDIR           specify one or more rules directories using one or
                        more -r arguments. Any -r flags override the default
                        rules in /usr/lib/python3/dist-
                        packages/ansiblelint/rules, unless -R is also used.
  -R                    Use default rules in /usr/lib/python3/dist-
                        packages/ansiblelint/rules in addition to any extra
                        rules directories specified with -r. There is no need
                        to specify this if no -r flags are used
  -t TAGS               only check rules whose id/tags match these values
  -T                    list all the tags
  -v                    Increase verbosity level
  -x SKIP_LIST          only check rules whose id/tags do not match these
                        values
  --nocolor             disable colored output
  --force-color         Try force colored output (relying on ansible's code)
  --exclude=EXCLUDE_PATHS
                        path to directories or files to skip. This option is
                        repeatable.
  -c C                  Specify configuration file to use.  Defaults to
                        ".ansible-lint"
/bin/bash: line 2: flake8: command not found
CRITICAL Lint failed with error code 127
WARNING  An error occurred during the test sequence action: 'lint'. Cleaning up.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > destroy
INFO     Sanity checks: 'docker'
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
ok: [localhost] => (item=centos_7)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```
</details>

2. Перейдите в каталог с ролью vector-role и создайте сценарий тестирования по умолчанию при помощи `molecule init scenario --driver-name docker`.
3. Добавьте несколько разных дистрибутивов (centos:8, ubuntu:latest) для инстансов и протестируйте роль, исправьте найденные ошибки, если они есть.
4. Добавьте несколько assert в verify.yml-файл для  проверки работоспособности vector-role (проверка, что конфиг валидный, проверка успешности запуска и др.). 
5. Запустите тестирование роли повторно и проверьте, что оно прошло успешно.
6. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

### Tox

1. Добавьте в директорию с vector-role файлы из [директории](./example).
2. Запустите `docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash`, где path_to_repo — путь до корня репозитория с vector-role на вашей файловой системе.
3. Внутри контейнера выполните команду `tox`, посмотрите на вывод.
5. Создайте облегчённый сценарий для `molecule` с драйвером `molecule_podman`. Проверьте его на исполнимость.
6. Пропишите правильную команду в `tox.ini`, чтобы запускался облегчённый сценарий.
8. Запустите команду `tox`. Убедитесь, что всё отработало успешно.
9. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

После выполнения у вас должно получится два сценария molecule и один tox.ini файл в репозитории. Не забудьте указать в ответе теги решений Tox и Molecule заданий. В качестве решения пришлите ссылку на  ваш репозиторий и скриншоты этапов выполнения задания.
