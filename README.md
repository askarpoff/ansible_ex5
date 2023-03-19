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

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/resources/playbooks/converge.yml
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > create
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Create] ******************************************************************

TASK [Log into a Docker registry] **********************************************
skipping: [localhost] => (item=None)
skipping: [localhost]

TASK [Check presence of custom Dockerfiles] ************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/clickhouse/centos_7/Dockerfile_centos_7', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679244944.0444648-57174-210431815018422/source', 'md5sum': 'e90d08cd34f49a5f8a41a07de1348618', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2199, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679244944.0444648-57174-210431815018422/source', 'dest': '/home/debian/.cache/molecule/clickhouse/centos_7/Dockerfile_centos_7', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
ok: [localhost] => (item=molecule_local/centos:7)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '284724598364.57319', 'results_file': '/home/debian/.ansible_async/284724598364.57319', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=7    changed=3    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Apply Clickhouse Role] ***************************************************
ERROR! the role 'ansible-clickhouse' was not found in /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/resources/playbooks/roles:/home/debian/.cache/molecule/clickhouse/centos_7/roles:/home/debian/ansible_ex5/playbook/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles:/home/debian/ansible_ex5/playbook/roles/clickhouse:/home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/resources/playbooks

The error appears to be in '/home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/resources/playbooks/converge.yml': line 7, column 15, but may
be elsewhere in the file depending on the exact syntax problem.

The offending line appears to be:

      include_role:
        name: ansible-clickhouse
              ^ here

PLAY RECAP *********************************************************************
centos_7                   : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

CRITICAL Ansible return code was 2, command was: ['ansible-playbook', '-D', '--inventory', '/home/debian/.cache/molecule/clickhouse/centos_7/inventory', '--skip-tags', 'molecule-notest,notest', '/home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/resources/playbooks/converge.yml']
WARNING  An error occurred during the test sequence action: 'converge'. Cleaning up.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > destroy
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
changed: [localhost] => (item=centos_7)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```
</details>

2. Перейдите в каталог с ролью vector-role и создайте сценарий тестирования по умолчанию при помощи `molecule init scenario --driver-name docker`.
```bash
debian@debian:~/ansible_ex5/playbook/roles/vector-role$ molecule init scenario --driver-name docker
INFO     Initializing new scenario default...
INFO     Initialized scenario in /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default successfully.
```
3. Добавьте несколько разных дистрибутивов (centos:8, ubuntu:latest) для инстансов и протестируйте роль, исправьте найденные ошибки, если они есть
<details>
<summary>molecule test -s default</summary>
  ```bash
  debian@debian:~/ansible_ex5/playbook/roles/vector-role$ molecule test -s default
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.
INFO     default scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/8902dd/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/8902dd/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/8902dd/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Running default > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Running default > lint
INFO     Lint is disabled.
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Running default > destroy
INFO     Sanity checks: 'docker'
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=instance)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Running default > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/converge.yml
INFO     Running default > create
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Create] ******************************************************************

TASK [Log into a Docker registry] **********************************************
skipping: [localhost] => (item=None)
skipping: [localhost]

TASK [Check presence of custom Dockerfiles] ************************************
ok: [localhost] => (item={'image': 'docker.io/pycontribs/centos:8', 'name': 'instance', 'pre_build_image': True})

TASK [Create Dockerfiles from image names] *************************************
skipping: [localhost] => (item={'image': 'docker.io/pycontribs/centos:8', 'name': 'instance', 'pre_build_image': True})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'changed': False, 'skipped': True, 'skip_reason': 'Conditional result was False', 'item': {'image': 'docker.io/pycontribs/centos:8', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
skipping: [localhost] => (item=molecule_local/docker.io/pycontribs/centos:8)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'image': 'docker.io/pycontribs/centos:8', 'name': 'instance', 'pre_build_image': True})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '44346259124.59445', 'results_file': '/home/debian/.ansible_async/44346259124.59445', 'changed': True, 'failed': False, 'item': {'image': 'docker.io/pycontribs/centos:8', 'name': 'instance', 'pre_build_image': True}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=5    changed=2    unreachable=0    failed=0    skipped=4    rescued=0    ignored=0

INFO     Running default > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Running default > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [instance]

TASK [Include vector-role] *****************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
changed: [instance]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [instance]

TASK [vector-role : Install Vector packages | CentOS] **************************
fatal: [instance]: FAILED! => {"changed": false, "msg": "Failed to download metadata for repo 'appstream': Cannot prepare internal mirrorlist: No URLs in mirrorlist", "rc": 1, "results": []}

PLAY RECAP *********************************************************************
instance                   : ok=2    changed=1    unreachable=0    failed=1    skipped=1    rescued=0    ignored=0

CRITICAL Ansible return code was 2, command was: ['ansible-playbook', '--inventory', '/home/debian/.cache/molecule/vector-role/default/inventory', '--skip-tags', 'molecule-notest,notest', '/home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/converge.yml']
WARNING  An error occurred during the test sequence action: 'converge'. Cleaning up.
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Running default > destroy
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=instance)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=instance)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```
</details>
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
