Role Name
=========

Ansible role to install python 2/3

Requirements
------------

Tested on ansible 2.2. Should be fine for >= 2.1

Role Variables
--------------
```yaml
temp_dir: "/tmp"

working_dir: "/tmp"

install_dir: "/usr/local"

pip_url: "https://bootstrap.pypa.io/get-pip.py"

default_pip_packages:
  - "pip"
  - "setuptools"

python_versions:
  python3:
    version: 3.6
    release: 3.6.2
    py_link: python3.6
    py_name: python3
    pip_link: pip3.6
    pip_name: pip3

  python2:
    version: 2.7
    release: 2.7.13 
    py_link: python2.7
    py_name: python2 
    pip_link: pip2.7
    pip_name: pip2
```

Dependencies
------------

None

Example Playbook
----------------

```yaml
---
- name: Build Python
  hosts: somehost
  become: True
  roles:
    - { role: ansible-python }
```

License
-------

GPLv3

Author Information
------------------

Brad Searle - codingpackets.com
