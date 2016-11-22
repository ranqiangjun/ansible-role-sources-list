Ansible Role: ranqiangjun.sources-list
=========

Replace the default /etc/apt/sources.list with a new and fast one generated from https://repogen.simplylinux.ch/. Useful for network limited country like China

Role Variables
--------------

- sources_list_sources_list_url: https://repogen.simplylinux.ch/txt/trusty/sources_552b4d46c8b4014a31f68adbf647498e359b3d04.txt
- sources_list_gpg_keys_url: https://repogen.simplylinux.ch/txt/trusty/gpg_552b4d46c8b4014a31f68adbf647498e359b3d04.txt
- sources_list_use_local_files: true
- sources_list_country: cn
- sources_list_backup: yes


Example Playbook
----------------


~~~
- hosts: test
  vars:
    sources_list_use_local_files: false
  gather_facts: false
  become: yes
  roles:
    - ranqiangjun.sources-list
~~~

License
-------

GPLv3

Author Information
------------------

Qiangjun Ran (jungle) http://ranqiangjun.com
