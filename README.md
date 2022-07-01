ansible-vector-role
=========
Ansible Role to install Vector. Vector is a high-performance, end-to-end (agent & aggregator) observability data pipeline that puts you in control of your observability data.

Requirements
------------
The role use the unzip application. You should install unzip in ansible pre-task. 

Role Variables
--------------
F: You can specify a particular vector ersion 
```
vector_version: "0.22.0"
```

Dependencies
------------
-

Example Playbook
----------------
```
- name: Install VECTOR
  hosts: vector-01
  tags: vector
  pre_tasks:
  - name: Install UnZIP by apt
    become: true
    ansible.builtin.apt:
      package: "{{ item }}"
    with_items:
      - unzip
  roles:
    - vector

```
License
-------

BSD

Author Information
------------------

AirDRoN

