# ansible_ex5

### Molecule

1. Запустите  `molecule test -s centos_7` внутри корневой директории clickhouse-role, посмотрите на вывод команды. Данная команда может отработать с ошибками, это нормально. Наша цель - посмотреть как другие в реальном мире используют молекулу.
<details>
<summary>molecule test -s centos_7</summary>  
  
```bash 
molecule test -s centos_7
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
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/clickhouse/centos_7/Dockerfile_centos_7', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679813623.7486277-111015-224949230274010/source', 'md5sum': 'e90d08cd34f49a5f8a41a07de1348618', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2199, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679813623.7486277-111015-224949230274010/source', 'dest': '/home/debian/.cache/molecule/clickhouse/centos_7/Dockerfile_centos_7', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
ok: [localhost] => (item=molecule_local/centos:7)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '324242951719.111159', 'results_file': '/home/debian/.ansible_async/324242951719.111159', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

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

TASK [clickhouse : Include OS Family Specific Variables] ***********************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/precheck.yml for centos_7

TASK [clickhouse : Requirements check | Checking sse4_2 support] ***************
ok: [centos_7]

TASK [clickhouse : Requirements check | Not supported distribution && release] ***
skipping: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/params.yml for centos_7

TASK [clickhouse : Set clickhouse_service_enable] ******************************
ok: [centos_7]

TASK [clickhouse : Set clickhouse_service_ensure] ******************************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/install/yum.yml for centos_7

TASK [clickhouse : Install by YUM | Ensure clickhouse repo GPG key imported] ***
changed: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse repo installed] **********
--- before: /etc/yum.repos.d/clickhouse.repo
+++ after: /etc/yum.repos.d/clickhouse.repo
@@ -0,0 +1,8 @@
+[clickhouse]
+async = 1
+baseurl = https://repo.clickhouse.tech/rpm/stable/x86_64/
+enabled = 1
+gpgcheck = 1
+gpgkey = https://repo.clickhouse.tech//CLICKHOUSE-KEY.GPG
+name = Clickhouse repo
+

changed: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (latest)] ***
changed: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (version latest)] ***
skipping: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/sys.yml for centos_7

TASK [clickhouse : Check clickhouse config, data and logs] *********************
ok: [centos_7] => (item=/var/log/clickhouse-server)
--- before
+++ after
@@ -1,4 +1,4 @@
 {
-    "mode": "0700",
+    "mode": "0770",
     "path": "/etc/clickhouse-server"
 }

changed: [centos_7] => (item=/etc/clickhouse-server)
--- before
+++ after
@@ -1,7 +1,7 @@
 {
-    "group": 0,
-    "mode": "0755",
-    "owner": 0,
+    "group": 996,
+    "mode": "0770",
+    "owner": 999,
     "path": "/var/lib/clickhouse/tmp/",
-    "state": "absent"
+    "state": "directory"
 }

changed: [centos_7] => (item=/var/lib/clickhouse/tmp/)
--- before
+++ after
@@ -1,4 +1,4 @@
 {
-    "mode": "0700",
+    "mode": "0770",
     "path": "/var/lib/clickhouse/"
 }

changed: [centos_7] => (item=/var/lib/clickhouse/)

TASK [clickhouse : Config | Create config.d folder] ****************************
--- before
+++ after
@@ -1,4 +1,4 @@
 {
-    "mode": "0500",
+    "mode": "0770",
     "path": "/etc/clickhouse-server/config.d"
 }

changed: [centos_7]

TASK [clickhouse : Config | Create users.d folder] *****************************
--- before
+++ after
@@ -1,4 +1,4 @@
 {
-    "mode": "0500",
+    "mode": "0770",
     "path": "/etc/clickhouse-server/users.d"
 }

changed: [centos_7]

TASK [clickhouse : Config | Generate system config] ****************************
--- before
+++ after: /home/debian/.ansible/tmp/ansible-local-111318fzqekk4m/tmp_qi35tl2/config.j2
@@ -0,0 +1,381 @@
+<?xml version="1.0"?>
+<!--
+ -
+ - Ansible managed: Do NOT edit this file manually!
+ -
+-->
+<clickhouse>
+    <logger>
+        <!-- Possible levels: https://github.com/pocoproject/poco/blob/develop/Foundation/include/Poco/Logger.h#L105 -->
+        <level>trace</level>
+        <log>/var/log/clickhouse-server/clickhouse-server.log</log>
+        <errorlog>/var/log/clickhouse-server/clickhouse-server.err.log</errorlog>
+        <size>1000M</size>
+        <count>10</count>
+    </logger>
+
+    <http_port>8123</http_port>
+
+    <tcp_port>9000</tcp_port>
+
+    <!-- Used with https_port and tcp_port_secure. Full ssl options list: https://github.com/ClickHouse-Extras/poco/blob/master/NetSSL_OpenSSL/include/Poco/Net/SSLManager.h#L71 -->
+    <openSSL>
+        <server> <!-- Used for https server AND secure tcp port -->
+            <!-- openssl req -subj "/CN=localhost" -new -newkey rsa:2048 -days 365 -nodes -x509 -keyout /etc/clickhouse-server/server.key -out /etc/clickhouse-server/server.crt -->
+            <certificateFile>/etc/clickhouse-server/server.crt</certificateFile>
+            <privateKeyFile>/etc/clickhouse-server/server.key</privateKeyFile>
+            <!-- openssl dhparam -out /etc/clickhouse-server/dhparam.pem 4096 -->
+            <dhParamsFile>/etc/clickhouse-server/dhparam.pem</dhParamsFile>
+            <verificationMode>none</verificationMode>
+            <loadDefaultCAFile>true</loadDefaultCAFile>
+            <cacheSessions>true</cacheSessions>
+            <disableProtocols>sslv2,sslv3</disableProtocols>
+            <preferServerCiphers>true</preferServerCiphers>
+        </server>
+
+        <client> <!-- Used for connecting to https dictionary source -->
+            <loadDefaultCAFile>true</loadDefaultCAFile>
+            <cacheSessions>true</cacheSessions>
+            <disableProtocols>sslv2,sslv3</disableProtocols>
+            <preferServerCiphers>true</preferServerCiphers>
+            <!-- Use for self-signed: <verificationMode>none</verificationMode> -->
+            <invalidCertificateHandler>
+                <!-- Use for self-signed: <name>AcceptCertificateHandler</name> -->
+                <name>RejectCertificateHandler</name>
+            </invalidCertificateHandler>
+        </client>
+    </openSSL>
+
+    <!-- Default root page on http[s] server. For example load UI from https://tabix.io/ when opening http://localhost:8123 -->
+    <!--
+    <http_server_default_response><![CDATA[<html ng-app="SMI2"><head><base href="http://ui.tabix.io/"></head><body><div ui-view="" class="content-ui"></div><script src="http://loader.tabix.io/master.js"></script></body></html>]]></http_server_default_response>
+    -->
+
+    <!-- Port for communication between replicas. Used for data exchange. -->
+    <interserver_http_port>9009</interserver_http_port>
+
+
+
+    <!-- Hostname that is used by other replicas to request this server.
+         If not specified, than it is determined analoguous to 'hostname -f' command.
+         This setting could be used to switch replication to another network interface.
+      -->
+    <!--
+    <interserver_http_host>example.clickhouse.com</interserver_http_host>
+    -->
+
+    <!-- Listen specified host. use :: (wildcard IPv6 address), if you want to accept connections both with IPv4 and IPv6 from everywhere. -->
+    <!-- <listen_host>::</listen_host> -->
+    <!-- Same for hosts with disabled ipv6: -->
+    <!-- <listen_host>0.0.0.0</listen_host> -->
+    <listen_host>127.0.0.1</listen_host>
+
+    <max_connections>2048</max_connections>
+    <keep_alive_timeout>3</keep_alive_timeout>
+
+    <!-- Maximum number of concurrent queries. -->
+    <max_concurrent_queries>100</max_concurrent_queries>
+
+    <!-- Set limit on number of open files (default: maximum). This setting makes sense on Mac OS X because getrlimit() fails to retrieve
+         correct maximum value. -->
+    <!-- <max_open_files>262144</max_open_files> -->
+
+    <!-- Size of cache of uncompressed blocks of data, used in tables of MergeTree family.
+         In bytes. Cache is single for server. Memory is allocated only on demand.
+         Cache is used when 'use_uncompressed_cache' user setting turned on (off by default).
+         Uncompressed cache is advantageous only for very short queries and in rare cases.
+      -->
+    <uncompressed_cache_size>8589934592</uncompressed_cache_size>
+
+    <!-- Approximate size of mark cache, used in tables of MergeTree family.
+         In bytes. Cache is single for server. Memory is allocated only on demand.
+         You should not lower this value.
+      -->
+    <mark_cache_size>5368709120</mark_cache_size>
+
+
+    <!-- Path to data directory, with trailing slash. -->
+    <path>/var/lib/clickhouse/</path>
+
+    <!-- Path to temporary data for processing hard queries. -->
+    <tmp_path>/var/lib/clickhouse/tmp/</tmp_path>
+
+    <!-- Directory with user provided files that are accessible by 'file' table function. -->
+    <user_files_path>/var/lib/clickhouse/user_files/</user_files_path>
+
+    <!-- Path to configuration file with users, access rights, profiles of settings, quotas. -->
+    <users_config>users.xml</users_config>
+
+    <!-- Default profile of settings. -->
+    <default_profile>default</default_profile>
+
+    <!-- System profile of settings. This settings are used by internal processes (Buffer storage, Distibuted DDL worker and so on). -->
+    <!-- <system_profile>default</system_profile> -->
+
+    <!-- Default database. -->
+    <default_database>default</default_database>
+
+    <!-- Server time zone could be set here.
+
+         Time zone is used when converting between String and DateTime types,
+          when printing DateTime in text formats and parsing DateTime from text,
+          it is used in date and time related functions, if specific time zone was not passed as an argument.
+
+         Time zone is specified as identifier from IANA time zone database, like UTC or Africa/Abidjan.
+         If not specified, system time zone at server startup is used.
+
+         Please note, that server could display time zone alias instead of specified name.
+         Example: W-SU is an alias for Europe/Moscow and Zulu is an alias for UTC.
+    -->
+    <!-- <timezone>Europe/Moscow</timezone> -->
+
+    <!-- You can specify umask here (see "man umask"). Server will apply it on startup.
+         Number is always parsed as octal. Default umask is 027 (other users cannot read logs, data files, etc; group can only read).
+    -->
+    <!-- <umask>022</umask> -->
+
+    <!-- Perform mlockall after startup to lower first queries latency
+          and to prevent clickhouse executable from being paged out under high IO load.
+         Enabling this option is recommended but will lead to increased startup time for up to a few seconds.
+    -->
+    <mlock_executable>False</mlock_executable>
+
+    <!-- Configuration of clusters that could be used in Distributed tables.
+         https://clickhouse.com/docs/en/engines/table-engines/special/distributed/
+      -->
+    <remote_servers incl="clickhouse_remote_servers" />
+
+
+    <!-- If element has 'incl' attribute, then for it's value will be used corresponding substitution from another file.
+         By default, path to file with substitutions is /etc/metrika.xml. It could be changed in config in 'include_from' element.
+         Values for substitutions are specified in /clickhouse/name_of_substitution elements in that file.
+      -->
+
+    <!-- ZooKeeper is used to store metadata about replicas, when using Replicated tables.
+         Optional. If you don't use replicated tables, you could omit that.
+
+         See https://clickhouse.com/docs/en/engines/table-engines/mergetree-family/replication/
+      -->
+    <zookeeper incl="zookeeper-servers" optional="true" />
+
+    <!-- Substitutions for parameters of replicated tables.
+          Optional. If you don't use replicated tables, you could omit that.
+         See https://clickhouse.com/docs/en/engines/table-engines/mergetree-family/replication/#creating-replicated-tables
+      -->
+    <macros incl="macros" optional="true" />
+
+
+    <!-- Reloading interval for embedded dictionaries, in seconds. Default: 3600. -->
+    <builtin_dictionaries_reload_interval>3600</builtin_dictionaries_reload_interval>
+
+    <!-- If true, dictionaries are created lazily on first use. Otherwise they are initialised on server startup. Default: true -->
+    <!-- See also: https://clickhouse.com/docs/en/operations/server-configuration-parameters/settings/#server_configuration_parameters-dictionaries_lazy_load -->
+    <dictionaries_lazy_load>True</dictionaries_lazy_load>
+
+    <!-- Maximum session timeout, in seconds. Default: 3600. -->
+    <max_session_timeout>3600</max_session_timeout>
+
+    <!-- Default session timeout, in seconds. Default: 60. -->
+    <default_session_timeout>60</default_session_timeout>
+
+    <!-- Sending data to Graphite for monitoring. Several sections can be defined. -->
+    <!--
+        interval - send every X second
+        root_path - prefix for keys
+        hostname_in_path - append hostname to root_path (default = true)
+        metrics - send data from table system.metrics
+        events - send data from table system.events
+        asynchronous_metrics - send data from table system.asynchronous_metrics
+    -->
+    <!--
+    <graphite>
+        <host>localhost</host>
+        <port>42000</port>
+        <timeout>0.1</timeout>
+        <interval>60</interval>
+        <root_path>one_min</root_path>
+        <hostname_in_path>true</hostname_in_path>
+
+        <metrics>true</metrics>
+        <events>true</events>
+        <asynchronous_metrics>true</asynchronous_metrics>
+    </graphite>
+    <graphite>
+        <host>localhost</host>
+        <port>42000</port>
+        <timeout>0.1</timeout>
+        <interval>1</interval>
+        <root_path>one_sec</root_path>
+
+        <metrics>true</metrics>
+        <events>true</events>
+        <asynchronous_metrics>false</asynchronous_metrics>
+    </graphite>
+    -->
+
+
+    <!-- Query log. Used only for queries with setting log_queries = 1. -->
+    <query_log>
+        <!-- What table to insert data. If table is not exist, it will be created.
+             When query log structure is changed after system update,
+              then old table will be renamed and new table will be created automatically.
+        -->
+        <database>system</database>
+        <table>query_log</table>
+        <!--
+            PARTITION BY expr https://clickhouse.com/docs/en/table_engines/mergetree-family/custom_partitioning_key/
+            Example:
+                event_date
+                toMonday(event_date)
+                toYYYYMM(event_date)
+                toStartOfHour(event_time)
+        -->
+        <partition_by>toYYYYMM(event_date)</partition_by>
+        <!-- Interval of flushing data. -->
+        <flush_interval_milliseconds>7500</flush_interval_milliseconds>
+    </query_log>
+
+    <!-- Query thread log. Has information about all threads participated in query execution.
+         Used only for queries with setting log_query_threads = 1. -->
+    <query_thread_log>
+        <database>system</database>
+        <table>query_thread_log</table>
+        <partition_by>toYYYYMM(event_date)</partition_by>
+        <flush_interval_milliseconds>7500</flush_interval_milliseconds>
+    </query_thread_log>
+
+    <!-- Uncomment if use part log.
+         Part log contains information about all actions with parts in MergeTree tables (creation, deletion, merges, downloads).
+    <part_log>
+        <database>system</database>
+        <table>part_log</table>
+        <flush_interval_milliseconds>7500</flush_interval_milliseconds>
+    </part_log>
+    -->
+
+
+    <!-- Parameters for embedded dictionaries, used in Yandex.Metrica.
+         See https://clickhouse.com/docs/en/dicts/internal_dicts/
+    -->
+
+    <!-- Path to file with region hierarchy. -->
+    <!-- <path_to_regions_hierarchy_file>/opt/geo/regions_hierarchy.txt</path_to_regions_hierarchy_file> -->
+
+    <!-- Path to directory with files containing names of regions -->
+    <!-- <path_to_regions_names_files>/opt/geo/</path_to_regions_names_files> -->
+
+
+    <!-- Configuration of external dictionaries. See:
+         https://clickhouse.com/docs/en/sql-reference/dictionaries/external-dictionaries/external-dicts
+    -->
+    <dictionaries_config>*_dictionary.xml</dictionaries_config>
+
+    <!-- Uncomment if you want data to be compressed 30-100% better.
+         Don't do that if you just started using ClickHouse.
+      -->
+    <compression incl="clickhouse_compression">
+    <!--
+        <!- - Set of variants. Checked in order. Last matching case wins. If nothing matches, lz4 will be used. - ->
+        <case>
+
+            <!- - Conditions. All must be satisfied. Some conditions may be omitted. - ->
+            <min_part_size>10000000000</min_part_size>        <!- - Min part size in bytes. - ->
+            <min_part_size_ratio>0.01</min_part_size_ratio>   <!- - Min size of part relative to whole table size. - ->
+
+            <!- - What compression method to use. - ->
+            <method>zstd</method>
+        </case>
+    -->
+    </compression>
+
+    <!-- Allow to execute distributed DDL queries (CREATE, DROP, ALTER, RENAME) on cluster.
+         Works only if ZooKeeper is enabled. Comment it if such functionality isn't required. -->
+    <distributed_ddl>
+        <!-- Path in ZooKeeper to queue with DDL queries -->
+        <path>/clickhouse/task_queue/ddl</path>
+
+        <!-- Settings from this profile will be used to execute DDL queries -->
+        <!-- <profile>default</profile> -->
+    </distributed_ddl>
+
+    <!-- Settings to fine tune MergeTree tables. See documentation in source code, in MergeTreeSettings.h -->
+        <merge_tree>
+        </merge_tree>
+
+    <!-- Protection from accidental DROP.
+         If size of a MergeTree table is greater than max_table_size_to_drop (in bytes) than table could not be dropped with any DROP query.
+         If you want do delete one table and don't want to restart clickhouse-server, you could create special file <clickhouse-path>/flags/force_drop_table and make DROP once.
+         By default max_table_size_to_drop is 50GB; max_table_size_to_drop=0 allows to DROP any tables.
+         The same for max_partition_size_to_drop.
+         Uncomment to disable protection.
+    -->
+    <!-- <max_table_size_to_drop>0</max_table_size_to_drop> -->
+    <!-- <max_partition_size_to_drop>0</max_partition_size_to_drop> -->
+
+    <!-- Example of parameters for GraphiteMergeTree table engine -->
+    <graphite_rollup_example>
+        <pattern>
+            <regexp>click_cost</regexp>
+            <function>any</function>
+            <retention>
+                <age>0</age>
+                <precision>3600</precision>
+            </retention>
+            <retention>
+                <age>86400</age>
+                <precision>60</precision>
+            </retention>
+        </pattern>
+        <default>
+            <function>max</function>
+            <retention>
+                <age>0</age>
+                <precision>60</precision>
+            </retention>
+            <retention>
+                <age>3600</age>
+                <precision>300</precision>
+            </retention>
+            <retention>
+                <age>86400</age>
+                <precision>3600</precision>
+            </retention>
+        </default>
+    </graphite_rollup_example>
+
+
+    <!-- Exposing metrics data for scraping from Prometheus. -->
+    <!--
+        endpoint – HTTP endpoint for scraping metrics by prometheus server. Start from ‘/’.
+        port – Port for endpoint.
+        metrics – Flag that sets to expose metrics from the system.metrics table.
+        events – Flag that sets to expose metrics from the system.events table.
+        asynchronous_metrics – Flag that sets to expose current metrics values from the system.asynchronous_metrics table.
+    -->
+    <!--
+    <prometheus>
+        <endpoint>/metrics</endpoint>
+        <port>8001</port>
+        <metrics>true</metrics>
+        <events>true</events>
+        <asynchronous_metrics>true</asynchronous_metrics>
+    </prometheus>
+    -->
+
+
+    <!-- Directory in <clickhouse-path> containing schema files for various input formats.
+         The directory will be created if it doesn't exist.
+      -->
+    <format_schema_path>/var/lib/clickhouse//format_schemas/</format_schema_path>
+
+    <!-- Uncomment to disable ClickHouse internal DNS caching. -->
+    <!-- <disable_internal_dns_cache>1</disable_internal_dns_cache> -->
+
+    <kafka>
+    </kafka>
+
+
+
+
+
+</clickhouse>

changed: [centos_7]

TASK [clickhouse : Config | Generate users config] *****************************
--- before
+++ after: /home/debian/.ansible/tmp/ansible-local-111318fzqekk4m/tmp1iagdl3w/users.j2
@@ -0,0 +1,106 @@
+<?xml version="1.0"?>
+<!--
+ -
+ - Ansible managed: Do NOT edit this file manually!
+ -
+-->
+<clickhouse>
+   <profiles>
+    <!-- Profiles of settings. -->
+    <!-- Default profiles. -->
+        <default>
+            <max_memory_usage>10000000000</max_memory_usage>
+            <use_uncompressed_cache>0</use_uncompressed_cache>
+            <load_balancing>random</load_balancing>
+            <max_partitions_per_insert_block>100</max_partitions_per_insert_block>
+        </default>
+        <readonly>
+            <readonly>1</readonly>
+        </readonly>
+        <!-- Default profiles end. -->
+    <!-- Custom profiles. -->
+        <!-- Custom profiles end. -->
+    </profiles>
+
+    <!-- Users and ACL. -->
+    <users>
+    <!-- Default users. -->
+            <!-- Default user for login if user not defined -->
+        <default>
+                <password></password>
+                <networks incl="networks" replace="replace">
+                <ip>::1</ip>
+                <ip>127.0.0.1</ip>
+                </networks>
+        <profile>default</profile>
+        <quota>default</quota>
+            </default>
+            <!-- Example of user with readonly access -->
+        <readonly>
+                <password></password>
+                <networks incl="networks" replace="replace">
+                <ip>::1</ip>
+                <ip>127.0.0.1</ip>
+                </networks>
+        <profile>readonly</profile>
+        <quota>default</quota>
+            </readonly>
+        <!-- Custom users. -->
+            <!-- classic user with plain password -->
+        <testuser>
+                <password_sha256_hex>f2ca1bb6c7e907d06dafe4687e579fce76b37e4e93b7605022da52e6ccc26fd2</password_sha256_hex>
+                <networks incl="networks" replace="replace">
+                <ip>::1</ip>
+                <ip>127.0.0.1</ip>
+                </networks>
+        <profile>default</profile>
+        <quota>default</quota>
+                 <allow_databases>
+                    <database>testu1</database>
+                </allow_databases>
+                            </testuser>
+            <!-- classic user with hex password -->
+        <testuser2>
+                <password>testplpassword</password>
+                <networks incl="networks" replace="replace">
+                <ip>::1</ip>
+                <ip>127.0.0.1</ip>
+                </networks>
+        <profile>default</profile>
+        <quota>default</quota>
+                 <allow_databases>
+                    <database>testu2</database>
+                </allow_databases>
+                            </testuser2>
+            <!-- classic user with multi dbs and multi-custom network allow password -->
+        <testuser3>
+                <password>testplpassword</password>
+                <networks incl="networks" replace="replace">
+                <ip>192.168.0.0/24</ip>
+                <ip>10.0.0.0/8</ip>
+                </networks>
+        <profile>default</profile>
+        <quota>default</quota>
+                 <allow_databases>
+                    <database>testu1</database>
+                    <database>testu2</database>
+                    <database>testu3</database>
+                </allow_databases>
+                            </testuser3>
+        </users>
+
+    <!-- Quotas. -->
+    <quotas>
+        <!-- Default quotas. -->
+        <default>
+        <interval>
+        <duration>3600</duration>
+        <queries>0</queries>
+        <errors>0</errors>
+        <result_rows>0</result_rows>
+        <read_rows>0</read_rows>
+        <execution_time>0</execution_time>
+    </interval>
+        </default>
+            </quotas>
+</clickhouse>

changed: [centos_7]

TASK [clickhouse : Config | Generate remote_servers config] ********************
skipping: [centos_7]

TASK [clickhouse : Config | Generate macros config] ****************************
skipping: [centos_7]

TASK [clickhouse : Config | Generate zookeeper servers config] *****************
skipping: [centos_7]

TASK [clickhouse : Config | Fix interserver_http_port and intersever_https_port collision] ***
skipping: [centos_7]

TASK [clickhouse : Notify Handlers Now] ****************************************

RUNNING HANDLER [clickhouse : Restart Clickhouse Service] **********************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/service.yml for centos_7

TASK [clickhouse : Ensure clickhouse-server.service is enabled: True and state: restarted] ***
changed: [centos_7]

TASK [clickhouse : Wait for Clickhouse Server to Become Ready] *****************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/db.yml for centos_7

TASK [clickhouse : Set ClickHose Connection String] ****************************
ok: [centos_7]

TASK [clickhouse : Gather list of existing databases] **************************
ok: [centos_7]

TASK [clickhouse : Config | Delete database config] ****************************
skipping: [centos_7] => (item={'name': 'testu1'})
skipping: [centos_7] => (item={'name': 'testu2'})
skipping: [centos_7] => (item={'name': 'testu3'})
skipping: [centos_7] => (item={'name': 'testu4', 'state': 'absent'})

TASK [clickhouse : Config | Create database config] ****************************
changed: [centos_7] => (item={'name': 'testu1'})
changed: [centos_7] => (item={'name': 'testu2'})
changed: [centos_7] => (item={'name': 'testu3'})
skipping: [centos_7] => (item={'name': 'testu4', 'state': 'absent'})

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/dict.yml for centos_7

TASK [clickhouse : Config | Generate dictionary config] ************************
--- before
+++ after: /home/debian/.ansible/tmp/ansible-local-111318fzqekk4m/tmpdka8x26b/dicts.j2
@@ -0,0 +1,63 @@
+<?xml version="1.0"?>
+<!--
+ -
+ - Ansible managed: Do NOT edit this file manually!
+ -
+-->
+<clickhouse>
+ <dictionary>
+   <name>test_dict</name>
+   <source>
+    <odbc>
+     <connection_string>DSN=testdb</connection_string>
+     <table>dict_source</table>
+    </odbc>
+   </source>
+   <lifetime>
+     <min>300</min>
+     <max>360</max>
+   </lifetime>
+   <layout>
+     <hashed/>
+   </layout>
+   <structure>
+     <id>
+       <name>testIntKey</name>
+     </id>
+     <attribute>
+       <name>testAttrName</name>
+       <type>UInt32</type>
+       <null_value>0</null_value>
+     </attribute>
+   </structure>
+ </dictionary>
+ <dictionary>
+   <name>test_dict</name>
+   <source>
+    <odbc>
+     <connection_string>DSN=testdb</connection_string>
+     <table>dict_source</table>
+    </odbc>
+   </source>
+   <lifetime>
+     <min>300</min>
+     <max>360</max>
+   </lifetime>
+   <layout>
+     <complex_key_hashed/>
+   </layout>
+   <structure>
+     <key>
+     <attribute>
+       <name>testAttrComplexName</name>
+       <type>String</type>
+     </attribute>
+     </key>
+     <attribute>
+       <name>testAttrName</name>
+       <type>String</type>
+       <null_value></null_value>
+     </attribute>
+   </structure>
+ </dictionary>
+</clickhouse>

changed: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
skipping: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=27   changed=11   unreachable=0    failed=0    skipped=8    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > idempotence
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Apply Clickhouse Role] ***************************************************

TASK [clickhouse : Include OS Family Specific Variables] ***********************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/precheck.yml for centos_7

TASK [clickhouse : Requirements check | Checking sse4_2 support] ***************
ok: [centos_7]

TASK [clickhouse : Requirements check | Not supported distribution && release] ***
skipping: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/params.yml for centos_7

TASK [clickhouse : Set clickhouse_service_enable] ******************************
ok: [centos_7]

TASK [clickhouse : Set clickhouse_service_ensure] ******************************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/install/yum.yml for centos_7

TASK [clickhouse : Install by YUM | Ensure clickhouse repo GPG key imported] ***
ok: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse repo installed] **********
ok: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (latest)] ***
ok: [centos_7]

TASK [clickhouse : Install by YUM | Ensure clickhouse package installed (version latest)] ***
skipping: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/sys.yml for centos_7

TASK [clickhouse : Check clickhouse config, data and logs] *********************
ok: [centos_7] => (item=/var/log/clickhouse-server)
ok: [centos_7] => (item=/etc/clickhouse-server)
ok: [centos_7] => (item=/var/lib/clickhouse/tmp/)
ok: [centos_7] => (item=/var/lib/clickhouse/)

TASK [clickhouse : Config | Create config.d folder] ****************************
ok: [centos_7]

TASK [clickhouse : Config | Create users.d folder] *****************************
ok: [centos_7]

TASK [clickhouse : Config | Generate system config] ****************************
ok: [centos_7]

TASK [clickhouse : Config | Generate users config] *****************************
ok: [centos_7]

TASK [clickhouse : Config | Generate remote_servers config] ********************
skipping: [centos_7]

TASK [clickhouse : Config | Generate macros config] ****************************
skipping: [centos_7]

TASK [clickhouse : Config | Generate zookeeper servers config] *****************
skipping: [centos_7]

TASK [clickhouse : Config | Fix interserver_http_port and intersever_https_port collision] ***
skipping: [centos_7]

TASK [clickhouse : Notify Handlers Now] ****************************************

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/service.yml for centos_7

TASK [clickhouse : Ensure clickhouse-server.service is enabled: True and state: started] ***
ok: [centos_7]

TASK [clickhouse : Wait for Clickhouse Server to Become Ready] *****************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/db.yml for centos_7

TASK [clickhouse : Set ClickHose Connection String] ****************************
ok: [centos_7]

TASK [clickhouse : Gather list of existing databases] **************************
ok: [centos_7]

TASK [clickhouse : Config | Delete database config] ****************************
skipping: [centos_7] => (item={'name': 'testu1'})
skipping: [centos_7] => (item={'name': 'testu2'})
skipping: [centos_7] => (item={'name': 'testu3'})
skipping: [centos_7] => (item={'name': 'testu4', 'state': 'absent'})

TASK [clickhouse : Config | Create database config] ****************************
skipping: [centos_7] => (item={'name': 'testu1'})
skipping: [centos_7] => (item={'name': 'testu2'})
skipping: [centos_7] => (item={'name': 'testu3'})
skipping: [centos_7] => (item={'name': 'testu4', 'state': 'absent'})

TASK [clickhouse : include_tasks] **********************************************
included: /home/debian/ansible_ex5/playbook/roles/clickhouse/tasks/configure/dict.yml for centos_7

TASK [clickhouse : Config | Generate dictionary config] ************************
ok: [centos_7]

TASK [clickhouse : include_tasks] **********************************************
skipping: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=25   changed=0    unreachable=0    failed=0    skipped=9    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/clickhouse/molecule/centos_7/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/clickhouse/centos_7/inventory/host_vars
INFO     Running centos_7 > verify
INFO     Running Ansible Verifier
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [centos_7] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
centos_7                   : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
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
INFO     default scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/8902dd/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/8902dd/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/8902dd/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > lint
COMMAND: yamllint .
ansible-lint
flake8

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
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > destroy
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

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/converge.yml
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
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
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/vector-role/default/Dockerfile_centos_7', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679829900.3623652-1433-276300438759388/source', 'md5sum': 'e90d08cd34f49a5f8a41a07de1348618', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2199, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679829900.3623652-1433-276300438759388/source', 'dest': '/home/debian/.cache/molecule/vector-role/default/Dockerfile_centos_7', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
ok: [localhost] => (item=molecule_local/centos:7)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '58384923933.1586', 'results_file': '/home/debian/.ansible_async/58384923933.1586', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=7    changed=3    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Include vector-role] *****************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
changed: [centos_7]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_7]

TASK [vector-role : Install Vector packages | CentOS] **************************
changed: [centos_7]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_7]

TASK [vector-role : Creates directory] *****************************************
--- before
+++ after
@@ -1,7 +1,7 @@
 {
-    "group": 0,
-    "mode": "0755",
-    "owner": 0,
+    "group": 998,
+    "mode": "0644",
+    "owner": 1000,
     "path": "/var/lib/vector/local_logs",
-    "state": "absent"
+    "state": "directory"
 }

changed: [centos_7]

TASK [vector-role : Start Vector service] **************************************
changed: [centos_7]

RUNNING HANDLER [vector-role : Start Vector service] ***************************
ok: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=6    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > idempotence
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Include vector-role] *****************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
ok: [centos_7]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_7]

TASK [vector-role : Install Vector packages | CentOS] **************************
ok: [centos_7]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_7]

TASK [vector-role : Creates directory] *****************************************
ok: [centos_7]

TASK [vector-role : Start Vector service] **************************************
ok: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=5    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > verify
INFO     Running Ansible Verifier
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [centos_7] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
centos_7                   : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > destroy
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
<details>
<summary>molecule test -s centos_8</summary>
  
```bash
debian@debian:~/ansible_ex5/playbook/roles/vector-role$ molecule test -s centos_8
INFO     centos_8 scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/8902dd/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/8902dd/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/8902dd/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > lint
COMMAND: yamllint .
ansible-lint
flake8

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
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > destroy
INFO     Sanity checks: 'docker'
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=centos_8)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
ok: [localhost] => (item=centos_8)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/resources/playbooks/converge.yml
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > create
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
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile_c8.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:8', 'name': 'centos_8', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile_c8.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:8', 'name': 'centos_8', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/vector-role/centos_8/Dockerfile_centos_8', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679831082.3130622-6274-191069527995625/source', 'md5sum': '2767b2df92ab085846edadd7b1e1246e', 'checksum': '7517f82ef33e7277fe4524a4d3ce4ba8e5f26543', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2397, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679831082.3130622-6274-191069527995625/source', 'dest': '/home/debian/.cache/molecule/vector-role/centos_8/Dockerfile_centos_8', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile_c8.j2', 'checksum': '7517f82ef33e7277fe4524a4d3ce4ba8e5f26543', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile_c8.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:8', 'name': 'centos_8', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
changed: [localhost] => (item=molecule_local/centos:8)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile_c8.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:8', 'name': 'centos_8', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=centos_8)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '357057013717.7328', 'results_file': '/home/debian/.ansible_async/357057013717.7328', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile_c8.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:8', 'name': 'centos_8', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=7    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_8]

TASK [Apple Vector Role] *******************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
changed: [centos_8]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_8]

TASK [vector-role : Install Vector packages | CentOS] **************************
changed: [centos_8]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_8]

TASK [vector-role : Creates directory] *****************************************
--- before
+++ after
@@ -1,7 +1,7 @@
 {
-    "group": 0,
-    "mode": "0755",
-    "owner": 0,
+    "group": 995,
+    "mode": "0644",
+    "owner": 1000,
     "path": "/var/lib/vector/local_logs",
-    "state": "absent"
+    "state": "directory"
 }

changed: [centos_8]

TASK [vector-role : Start Vector service] **************************************
changed: [centos_8]

RUNNING HANDLER [vector-role : Start Vector service] ***************************
ok: [centos_8]

PLAY RECAP *********************************************************************
centos_8                   : ok=6    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > idempotence
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_8]

TASK [Apple Vector Role] *******************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
ok: [centos_8]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_8]

TASK [vector-role : Install Vector packages | CentOS] **************************
ok: [centos_8]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_8]

TASK [vector-role : Creates directory] *****************************************
ok: [centos_8]

TASK [vector-role : Start Vector service] **************************************
ok: [centos_8]

PLAY RECAP *********************************************************************
centos_8                   : ok=5    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > verify
INFO     Running Ansible Verifier
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [centos_8] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
centos_8                   : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/centos_8/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/centos_8/inventory/host_vars
INFO     Running centos_8 > destroy
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=centos_8)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=centos_8)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
```
</details>
<details>
<summary>molecule test -s ubuntu</summary>
  
```bash
debian@debian:~/ansible_ex5/playbook/roles/vector-role$ molecule test -s ubuntu_latest
INFO     ubuntu_latest scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/8902dd/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/8902dd/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/8902dd/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > lint
COMMAND: yamllint .
ansible-lint
flake8

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
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > destroy
INFO     Sanity checks: 'docker'
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=ubuntu_latest)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
ok: [localhost] => (item=ubuntu_latest)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/resources/playbooks/converge.yml
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > create
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
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'sudo', 'container': 'docker'}, 'image': 'ubuntu:latest', 'name': 'ubuntu_latest', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'sudo', 'container': 'docker'}, 'image': 'ubuntu:latest', 'name': 'ubuntu_latest', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/vector-role/ubuntu_latest/Dockerfile_ubuntu_latest', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679832166.0865881-10305-280896454652656/source', 'md5sum': '494f081df668e1c263575fc6845e4a2e', 'checksum': 'f2a55a6b663585869c406d23ec64a6edf4c5a7aa', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2199, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679832166.0865881-10305-280896454652656/source', 'dest': '/home/debian/.cache/molecule/vector-role/ubuntu_latest/Dockerfile_ubuntu_latest', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': 'f2a55a6b663585869c406d23ec64a6edf4c5a7aa', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'sudo', 'container': 'docker'}, 'image': 'ubuntu:latest', 'name': 'ubuntu_latest', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
changed: [localhost] => (item=molecule_local/ubuntu:latest)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'sudo', 'container': 'docker'}, 'image': 'ubuntu:latest', 'name': 'ubuntu_latest', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=ubuntu_latest)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '56342474020.14762', 'results_file': '/home/debian/.ansible_async/56342474020.14762', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'sudo', 'container': 'docker'}, 'image': 'ubuntu:latest', 'name': 'ubuntu_latest', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=7    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [ubuntu_latest]

TASK [Apple Vector Role] *******************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
skipping: [ubuntu_latest]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
changed: [ubuntu_latest]

TASK [vector-role : Install Vector packages | CentOS] **************************
skipping: [ubuntu_latest]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
Selecting previously unselected package vector.
(Reading database ... 9553 files and directories currently installed.)
Preparing to unpack /tmp/vector_0.27.0-1_amd64.deb ...
Unpacking vector (0.27.0-1) ...
Setting up vector (0.27.0-1) ...
systemd-journal:x:101:
changed: [ubuntu_latest]

TASK [vector-role : Creates directory] *****************************************
--- before
+++ after
@@ -1,7 +1,7 @@
 {
-    "group": 0,
-    "mode": "0755",
-    "owner": 0,
+    "group": 999,
+    "mode": "0644",
+    "owner": 1000,
     "path": "/var/lib/vector/local_logs",
-    "state": "absent"
+    "state": "directory"
 }

changed: [ubuntu_latest]

TASK [vector-role : Start Vector service] **************************************
changed: [ubuntu_latest]

RUNNING HANDLER [vector-role : Start Vector service] ***************************
ok: [ubuntu_latest]

PLAY RECAP *********************************************************************
ubuntu_latest              : ok=6    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > idempotence
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [ubuntu_latest]

TASK [Apple Vector Role] *******************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
skipping: [ubuntu_latest]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
ok: [ubuntu_latest]

TASK [vector-role : Install Vector packages | CentOS] **************************
skipping: [ubuntu_latest]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
ok: [ubuntu_latest]

TASK [vector-role : Creates directory] *****************************************
ok: [ubuntu_latest]

TASK [vector-role : Start Vector service] **************************************
ok: [ubuntu_latest]

PLAY RECAP *********************************************************************
ubuntu_latest              : ok=5    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > verify
INFO     Running Ansible Verifier
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Verify] ******************************************************************

TASK [Example assertion] *******************************************************
ok: [ubuntu_latest] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
ubuntu_latest              : ok=1    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/group_vars
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/ubuntu_latest/../resources/inventory/host_vars/ linked to /home/debian/.cache/molecule/vector-role/ubuntu_latest/inventory/host_vars
INFO     Running ubuntu_latest > destroy
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=ubuntu_latest)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=ubuntu_latest)

TASK [Delete docker networks(s)] ***********************************************

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory

```
</details>

4. Добавьте несколько assert в verify.yml-файл для  проверки работоспособности vector-role (проверка, что конфиг валидный, проверка успешности запуска и др.). 

Добавил проверку наличия валидности конфига и проверку версии vector.
```ansible
---
- name: Verify
  hosts: all
  gather_facts: false
  vars:
    vector_config_path: /etc/vector/vector.toml
  tasks:
  - name: Get Vector version
    ansible.builtin.command: "vector --version"
    changed_when: false
    register: vector_version
  - name: Assert Vector instalation
    assert:
      that: "'{{ vector_version.rc }}' == '0'"
  - name: Validation Vector configuration
    ansible.builtin.command: "vector validate --no-environment --config-toml {{ vector_config_path }}"
    changed_when: false
    register: vector_validate
  - name: Assert Vector validate config
    assert:
      that: "'{{ vector_validate.rc }}' == '0'"
```
5. Запустите тестирование роли повторно и проверьте, что оно прошло успешно.
<details>
<summary>molecule test -s default</summary>

```bash
debian@debian:~/ansible_ex5/playbook/roles/vector-role$ molecule test -s default
INFO     default scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
INFO     Set ANSIBLE_LIBRARY=/home/debian/.cache/ansible-compat/8902dd/modules:/home/debian/.ansible/plugins/modules:/usr/share/ansible/plugins/modules
INFO     Set ANSIBLE_COLLECTIONS_PATH=/home/debian/.cache/ansible-compat/8902dd/collections:/home/debian/.ansible/collections:/usr/share/ansible/collections
INFO     Set ANSIBLE_ROLES_PATH=/home/debian/.cache/ansible-compat/8902dd/roles:/home/debian/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > lint
COMMAND: yamllint .
ansible-lint
flake8

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
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > destroy
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

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > syntax
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

playbook: /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/converge.yml
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
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
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create Dockerfiles from image names] *************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Discover local Docker images] ********************************************
ok: [localhost] => (item={'diff': [], 'dest': '/home/debian/.cache/molecule/vector-role/default/Dockerfile_centos_7', 'src': '/home/debian/.ansible/tmp/ansible-tmp-1679835218.9113638-28743-63503944706692/source', 'md5sum': 'e90d08cd34f49a5f8a41a07de1348618', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'changed': True, 'uid': 1000, 'gid': 1000, 'owner': 'debian', 'group': 'debian', 'mode': '0600', 'state': 'file', 'size': 2199, 'invocation': {'module_args': {'src': '/home/debian/.ansible/tmp/ansible-tmp-1679835218.9113638-28743-63503944706692/source', 'dest': '/home/debian/.cache/molecule/vector-role/default/Dockerfile_centos_7', 'mode': '0600', 'follow': False, '_original_basename': 'Dockerfile.j2', 'checksum': '4b70768619482424811f2977aa277a5acf2b13a1', 'backup': False, 'force': True, 'unsafe_writes': False, 'content': None, 'validate': None, 'directory_mode': None, 'remote_src': None, 'local_follow': None, 'owner': None, 'group': None, 'seuser': None, 'serole': None, 'selevel': None, 'setype': None, 'attributes': None}}, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item', 'i': 0, 'ansible_index_var': 'i'})

TASK [Build an Ansible compatible image (new)] *********************************
ok: [localhost] => (item=molecule_local/centos:7)

TASK [Create docker network(s)] ************************************************

TASK [Determine the CMD directives] ********************************************
ok: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Create molecule instance(s)] *********************************************
changed: [localhost] => (item=centos_7)

TASK [Wait for instance(s) creation to complete] *******************************
FAILED - RETRYING: Wait for instance(s) creation to complete (300 retries left).
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '40095340673.28886', 'results_file': '/home/debian/.ansible_async/40095340673.28886', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'ansible', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=7    changed=3    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > prepare
WARNING  Skipping, prepare playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > converge
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Include vector-role] *****************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
changed: [centos_7]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_7]

TASK [vector-role : Install Vector packages | CentOS] **************************
changed: [centos_7]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_7]

TASK [vector-role : Creates directory] *****************************************
--- before
+++ after
@@ -1,7 +1,7 @@
 {
-    "group": 0,
-    "mode": "0755",
-    "owner": 0,
+    "group": 998,
+    "mode": "0644",
+    "owner": 1000,
     "path": "/var/lib/vector/local_logs",
-    "state": "absent"
+    "state": "directory"
 }

changed: [centos_7]

TASK [vector-role : Start Vector service] **************************************
changed: [centos_7]

RUNNING HANDLER [vector-role : Start Vector service] ***************************
ok: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=6    changed=4    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > idempotence
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Converge] ****************************************************************

TASK [Gathering Facts] *********************************************************
ok: [centos_7]

TASK [Include vector-role] *****************************************************

TASK [vector-role : Get Vector distrib | CentOS] *******************************
ok: [centos_7]

TASK [vector-role : Get Vector distrib | Ubuntu] *******************************
skipping: [centos_7]

TASK [vector-role : Install Vector packages | CentOS] **************************
ok: [centos_7]

TASK [vector-role : Install Vector packages | Ubuntu] **************************
skipping: [centos_7]

TASK [vector-role : Creates directory] *****************************************
ok: [centos_7]

TASK [vector-role : Start Vector service] **************************************
ok: [centos_7]

PLAY RECAP *********************************************************************
centos_7                   : ok=5    changed=0    unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

INFO     Idempotence completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > side_effect
WARNING  Skipping, side effect playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > verify
INFO     Running Ansible Verifier
[DEPRECATION WARNING]: Ansible will require Python 3.8 or newer on the
controller starting with Ansible 2.12. Current version: 3.7.3 (default, Oct 31
2022, 14:04:00) [GCC 8.3.0]. This feature will be removed from ansible-core in
version 2.12. Deprecation warnings can be disabled by setting
deprecation_warnings=False in ansible.cfg.

PLAY [Verify] ******************************************************************

TASK [Get Vector version] ******************************************************
ok: [centos_7]

TASK [Assert Vector instalation] ***********************************************
ok: [centos_7] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Validation Vector configuration] *****************************************
ok: [centos_7]

TASK [Assert Vector validate config] *******************************************
ok: [centos_7] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
centos_7                   : ok=4    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Verifier completed successfully.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/hosts.yml linked to /home/debian/.cache/molecule/vector-role/default/inventory/hosts
INFO     Inventory /home/debian/ansible_ex5/playbook/roles/vector-role/molecule/default/../resources/inventory/group_vars/ linked to /home/debian/.cache/molecule/vector-role/default/inventory/group_vars
INFO     Running default > destroy
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

6. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

<a href='https://github.com/askarpoff/vector-role/releases/tag/1.1.0'> Ссылка на релиз</a>
### Tox

1. Добавьте в директорию с vector-role файлы из директории example.
2. Запустите `docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash`, где path_to_repo — путь до корня репозитория с vector-role на вашей файловой системе.
3. Внутри контейнера выполните команду `tox`, посмотрите на вывод.
![image](https://user-images.githubusercontent.com/108946489/227779016-93102a81-b492-41a4-8191-a9e75375f5d0.png)

Сделал свой compability сценарий, т.к. такого не было, c драйвером podman
<details>
  <summary>Вывод сценария</summary>
```bash
[root@34c6baac1e82 vector-role]#
tox
py37-ansible210 installed: ansible==2.10.7,ansible-base==2.10.17,ansible-compat==1.0.0,ansible-lint==5.1.3,arrow==1.2.3,bcrypt==4.0.1,binaryornot==0.4.4,bracex==2.3.post1,cached-property==1.5.2,Cerberus==1.3.2,certifi==2022.12.7,cffi==1.15.1,chardet==5.1.0,charset-normalizer==3.1.0,click==8.1.3,click-help-colors==0.9.1,cookiecutter==2.1.1,cryptography==40.0.1,distro==1.8.0,enrich==1.2.7,idna==3.4,importlib-metadata==6.1.0,Jinja2==3.1.2,jinja2-time==0.2.0,jmespath==1.0.1,lxml==4.9.2,markdown-it-py==2.2.0,MarkupSafe==2.1.2,mdurl==0.1.2,molecule==3.4.0,molecule-podman==1.0.1,packaging==23.0,paramiko==2.12.0,pathspec==0.11.1,pluggy==0.13.1,pycparser==2.21,Pygments==2.14.0,PyNaCl==1.5.0,python-dateutil==2.8.2,python-slugify==8.0.1,PyYAML==5.4.1,requests==2.28.2,rich==13.3.2,ruamel.yaml==0.17.21,ruamel.yaml.clib==0.2.7,selinux==0.2.1,six==1.16.0,subprocess-tee==0.3.5,tenacity==8.2.2,text-unidecode==1.3,typing_extensions==4.5.0,urllib3==1.26.15,wcmatch==8.4.1,yamllint==1.26.3,zipp==3.15.0
py37-ansible210 run-test-pre: PYTHONHASHSEED='547073935'
py37-ansible210 run-test: commands[0] | molecule test -s compability --destroy always
INFO     compability scenario test matrix: dependency, lint, cleanup, destroy, syntax, create, prepare, converge, idempotence, side_effect, verify, cleanup, destroy
INFO     Performing prerun...
WARNING  Failed to locate command: [Errno 2] No such file or directory: 'git': 'git'
INFO     Guessed /opt/vector-role as project root directory
WARNING  Computed fully qualified role name of askarpoff.vector-role does not follow current galaxy requirements.
Please edit meta/main.yml and assure we can correctly determine full role name:

galaxy_info:
role_name: my_name  # if absent directory name hosting role is used instead
namespace: my_galaxy_namespace  # if absent, author is used instead

Namespace: https://galaxy.ansible.com/docs/contributing/namespaces.html#galaxy-namespace-limitations
Role: https://galaxy.ansible.com/docs/contributing/creating_role.html#role-names

As an alternative, you can add 'role-name' to either skip_list or warn_list.

INFO     Using /root/.cache/ansible-lint/b984a4/roles/askarpoff.vector-role symlink to current repository in order to enable Ansible to find the role using its expected full name.
INFO     Added ANSIBLE_ROLES_PATH=~/.ansible/roles:/usr/share/ansible/roles:/etc/ansible/roles:/root/.cache/ansible-lint/b984a4/roles
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/hosts.yml linked to /root/.cache/molecule/vector-role/compability/inventory/hosts
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/group_vars/ linked to /root/.cache/molecule/vector-role/compability/inventory/group_vars
INFO     Running compability > dependency
WARNING  Skipping, missing the requirements file.
WARNING  Skipping, missing the requirements file.
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/hosts.yml linked to /root/.cache/molecule/vector-role/compability/inventory/hosts
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/group_vars/ linked to /root/.cache/molecule/vector-role/compability/inventory/group_vars
INFO     Running compability > lint
COMMAND: yamllint .
ansible-lint
flake8

./.tox/py37-ansible210/lib/python3.7/site-packages/ansible_collections/infinidat/infinibox/.gitlab-ci.yml
  34:10     error    too many spaces after hyphen  (hyphens)
  35:10     error    too many spaces after hyphen  (hyphens)
  36:10     error    too many spaces after hyphen  (hyphens)
  37:10     error    too many spaces after hyphen  (hyphens)
  38:10     error    too many spaces after hyphen  (hyphens)
  39:10     error    too many spaces after hyphen  (hyphens)

./.tox/py37-ansible210/lib/python3.7/site-packages/ansible_collections/infinidat/infinibox/playbooks/test_remove_resources.yml
  206:1     error    too many blank lines (2 > 0)  (empty-lines)

./.tox/py37-ansible210/lib/python3.7/site-packages/molecule/cookiecutter/scenario/verifier/ansible/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/verify.yml
  4:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible210/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/create.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible210/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/destroy.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible210/lib/python3.7/site-packages/molecule/cookiecutter/molecule/{{cookiecutter.role_name}}/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/molecule.yml
  8:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37/lib/python3.7/site-packages/molecule/cookiecutter/scenario/verifier/ansible/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/verify.yml
  4:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/create.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/destroy.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37/lib/python3.7/site-packages/molecule/cookiecutter/molecule/{{cookiecutter.role_name}}/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/molecule.yml
  8:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/ansible_collections/infinidat/infinibox/.gitlab-ci.yml
  34:10     error    too many spaces after hyphen  (hyphens)
  35:10     error    too many spaces after hyphen  (hyphens)
  36:10     error    too many spaces after hyphen  (hyphens)
  37:10     error    too many spaces after hyphen  (hyphens)
  38:10     error    too many spaces after hyphen  (hyphens)
  39:10     error    too many spaces after hyphen  (hyphens)

./.tox/py37-ansible30/lib/python3.7/site-packages/ansible_collections/infinidat/infinibox/playbooks/test_remove_resources.yml
  206:1     error    too many blank lines (2 > 0)  (empty-lines)

./.tox/py37-ansible30/lib/python3.7/site-packages/ansible_collections/community/sops/tests/integration/targets/lookup_sops/files/hidden-binary.yaml
  2:1       error    syntax error: found character '\t' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/ansible_collections/community/sops/tests/integration/targets/lookup_sops/files/hidden-json.yaml
  2:1       error    syntax error: found character '\t' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/molecule/cookiecutter/scenario/verifier/ansible/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/verify.yml
  4:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/create.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/molecule/cookiecutter/scenario/driver/delegated/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/destroy.yml
  2:2       error    syntax error: found character '%' that cannot start any token (syntax)

./.tox/py37-ansible30/lib/python3.7/site-packages/molecule/cookiecutter/molecule/{{cookiecutter.role_name}}/{{cookiecutter.molecule_directory}}/{{cookiecutter.scenario_name}}/molecule.yml
  8:2       error    syntax error: found character '%' that cannot start any token (syntax)

Failed to locate command: [Errno 2] No such file or directory: 'git': 'git'
WARNING  Computed fully qualified role name of askarpoff.vector-role does not follow current galaxy requirements.
Please edit meta/main.yml and assure we can correctly determine full role name:

galaxy_info:
role_name: my_name  # if absent directory name hosting role is used instead
namespace: my_galaxy_namespace  # if absent, author is used instead

Namespace: https://galaxy.ansible.com/docs/contributing/namespaces.html#galaxy-namespace-limitations
Role: https://galaxy.ansible.com/docs/contributing/creating_role.html#role-names

As an alternative, you can add 'role-name' to either skip_list or warn_list.

Traceback (most recent call last):
  File "/opt/vector-role/.tox/py37-ansible210/bin/ansible-lint", line 8, in <module>
    sys.exit(_run_cli_entrypoint())
  File "/opt/vector-role/.tox/py37-ansible210/lib/python3.7/site-packages/ansiblelint/__main__.py", line 299, in _run_cli_entrypoint
    sys.exit(main(sys.argv))
  File "/opt/vector-role/.tox/py37-ansible210/lib/python3.7/site-packages/ansiblelint/__main__.py", line 211, in main
    from ansiblelint.generate_docs import rules_as_rich, rules_as_rst, rules_as_str
  File "/opt/vector-role/.tox/py37-ansible210/lib/python3.7/site-packages/ansiblelint/generate_docs.py", line 6, in <module>
    from rich.console import render_group
ImportError: cannot import name 'render_group' from 'rich.console' (/opt/vector-role/.tox/py37-ansible210/lib/python3.7/site-packages/rich/console.py)
/bin/sh: line 2: flake8: command not found
CRITICAL Lint failed with error code 127
WARNING  An error occurred during the test sequence action: 'lint'. Cleaning up.
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/hosts.yml linked to /root/.cache/molecule/vector-role/compability/inventory/hosts
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/group_vars/ linked to /root/.cache/molecule/vector-role/compability/inventory/group_vars
INFO     Running compability > cleanup
WARNING  Skipping, cleanup playbook not configured.
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/hosts.yml linked to /root/.cache/molecule/vector-role/compability/inventory/hosts
INFO     Inventory /opt/vector-role/molecule/compability/../resources/inventory/group_vars/ linked to /root/.cache/molecule/vector-role/compability/inventory/group_vars
INFO     Running compability > destroy
INFO     Sanity checks: 'podman'

PLAY [Destroy] *****************************************************************

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item={'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'root', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'pre_build_image': True, 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']})

TASK [Wait for instance(s) deletion to complete] *******************************
changed: [localhost] => (item={'started': 1, 'finished': 0, 'ansible_job_id': '601403665813.450', 'results_file': '/root/.ansible_async/601403665813.450', 'changed': True, 'failed': False, 'item': {'capabilities': ['SYS_ADMIN'], 'command': '/usr/sbin/init', 'dockerfile': '../resources/Dockerfile.j2', 'env': {'ANSIBLE_USER': 'root', 'DEPLOY_GROUP': 'deployer', 'SUDO_GROUP': 'wheel', 'container': 'docker'}, 'image': 'centos:7', 'name': 'centos_7', 'pre_build_image': True, 'privileged': True, 'tmpfs': ['/run', '/tmp'], 'volumes': ['/sys/fs/cgroup:/sys/fs/cgroup']}, 'ansible_loop_var': 'item'})

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     Pruning extra files from scenario ephemeral directory
ERROR: InvocationError for command /opt/vector-role/.tox/py37-ansible210/bin/molecule test -s compability --destroy always (exited with code 1)
```
  </details>
4. Создайте облегчённый сценарий для `molecule` с драйвером `molecule_podman`. Проверьте его на исполнимость.

5. Пропишите правильную команду в `tox.ini`, чтобы запускался облегчённый сценарий.
6. Запустите команду `tox`. Убедитесь, что всё отработало успешно.
7. Добавьте новый тег на коммит с рабочим сценарием в соответствии с семантическим версионированием.

После выполнения у вас должно получится два сценария molecule и один tox.ini файл в репозитории. Не забудьте указать в ответе теги решений Tox и Molecule заданий. В качестве решения пришлите ссылку на  ваш репозиторий и скриншоты этапов выполнения задания.
