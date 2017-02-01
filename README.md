Ansible template with Galaxy [![Build Status](https://travis-ci.org/ewypych/ansible_template_galaxy.svg?branch=master)](https://travis-ci.org/ewypych/ansible_template_galaxy)
=========


This role allow ansible newbies to create a standard project structure as explain below with optionally install Galaxy Roles
> [Ansible best practices ](http://docs.ansible.com/ansible/playbooks_best_practices.html)

Requirements
------------

none

Role Variables
--------------
```
bpath = the path of where the role structure will be generated (default=/tmp/ansible_project/)
brole = the name of the generated role (default=common)
bgalaxy = the name of the Galaxy Role(s) which you want to install (default=ewypych.ansible_template)
```

Dependencies
------------
none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: localhost
  roles:
    - { role: ewypych.project_template, bpath: '/home/usr/devops-project', brole: 'samplerole', bgalaxy: 'boufnichel.project_template' }
```

Also you can install more Galaxy Roles than one, for example:

```
- hosts: localhost
  roles:
    - { role: ewypych.project_template, bpath: '/home/usr/devops-project', brole: 'samplerole', bgalaxy: ['ewypych.ansible_template', 'boufnichel.project_template'] }
```

License
-------

This Role was created as a fork of the [boufnichel.project_template](https://galaxy.ansible.com/boufnichel/project_template/). It contains following changes:

- installation of Galaxy Roles was added,
- now Role creates also the group_vars and host_vars catalogs
- files to copy were changed to templates
- default vars were changed

[GNU General Public License v3.0](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))

Author Information
------------------
[Emil Wypych](https://emilwypych.com)




