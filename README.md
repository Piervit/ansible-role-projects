Ansible Role - Project
======================

A project role for elao symfony standard vagrant box


Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian


Role Variables
--------------

    elao_projects:    # Array of projects
      foo:              # Project name
        type:  symfony  # Project type (php|silex|symfony|www)
        host:  foo.dev  # Project host
        root:  null     # Project root
        cache: null     # Project cache (symfony type only)
        logs:  null     # Project logs  (symfony type only)


Example Playbook
----------------

    - hosts: servers
      vars:
        elao_projects:
          foo: { type: symfony, host: foo.dev }
          bar: { type: silex, host: bar.dev }
      roles:
         - { role: elao.project, type: symfony }


License
-------

MIT


Author Information
------------------

http://www.elao.com/
