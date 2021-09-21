Role Name
=========

mcafee role can be used to install mcafee agent in redhat linux and windows.

Requirements
------------

extra variables `env` need to be mentioned.


Role Variables
--------------

Following variables to be set when new mcafee agent packages available.

```
redhat:
  installable: <package_name>.zip
  checksum: sha1:<checksum_here>

windows:
  installable: <package_name>.exe
  product_id: '{<product_id_here>}'
  checksum: <checksum_here>
  checksum_algorithm: sha1
```


Dependencies
------------

No dependency.

Example Playbook
----------------


    - hosts: servers
      roles:
         - mcafee

ansible-playbook playbook.yml -e env=<env_name>

env_name can be:
1. nonprod
2. prod