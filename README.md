Ansible Role - Project
======================

A project role for elao symfony standard vagrant box

Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian

Role Variables
--------------

* type: Project type (php|silex|symfony|www)
* name: Project name
* template: (optionnal) Nginx vhost template
* root: (optionnal) Project root path
* cache: (optionnal) Cache path
* logs: (optionnal) Logs path

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: elao.project, type: symfony }

License
-------

MIT

Author Information
------------------

http://www.elao.com/
