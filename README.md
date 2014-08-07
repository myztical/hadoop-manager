Role Name
========

"hadoop-manager":

Is a role that can be used to provision distribution inpependent hadoop cluster and orchestrate it.


Requirements
------------

- wget
- Java (see: http://wiki.apache.org/hadoop/HadoopJavaVersions )
- Jsvc
- JAVA_HOME variable must be set
- JSVC_HOME variable must be set 

Role Variables
--------------

Can be found in: "vars/main.yml"

- java_home: "{{ lookup('env', 'JAVA_HOME')  }}"
- jsvc_home: "{{ lookup('env', 'JSVC_HOME')  }}"
- hostfile: '{{ inventory_dir }}/{{ inventory_file }}'
- install_directory: /opt/
- distribution_link: http://apache.mesi.com.ar/hadoop/common/hadoop-2.4.1/hadoop-2.4.1.tar.gz
- datanode_data_dir: "file:///var/datanode_data"
- namenode_name_dir: "file:///tmp/namenode_name"
- namenode_local_dirs: "file:///tmp/namenode_local"
- namenode_log_dirs: "file:///var/log/"
- nodemanager_local_dirs: "file:///var/nodemanager_local"
- nodemanager_log_dirs: "file:///log/"

Role Default Values
--------------

Can be found in: "defaults/main.yml"
  - hdfs_user_pass: "hdfs"
  - yarn_user_pass: "yarn"
  - mapred_user_pass: "mapred"

Dependencies
------------

No dependencies.

Example Playbook
-------------------------

See: example_site.yml and example_inventory.ini, that are shipped with a role.

License
-------

GPLv2

Author Information
------------------

Serge C.

email: sergiy.chernyshow 'at' gmail
