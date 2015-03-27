Ansible Role - Projects
=======================

A projects role for elao symfony standard vagrant box


Requirements
------------

This role only run on elao symfony standard vagrant box. See https://vagrantcloud.com/elao/symfony-standard-debian


Role Variables
--------------

    elao_projects:    # Array of projects
      -
        name:           foo         # Project name
        index:          app         # Project index (symfony type only)
        type:           symfony     # Project type (php|silex|symfony|www|proxy)
        address:        "127.0.0.1" # Network address to listen (Web server configuration)
        port:           80          # Port to listen (Web server configuration)
        host:           foo.dev     # Project host
        root:           null        # Project root
        extra:          null        # Project extra configuration
        location_extra: null        # Project extra location configuration
        cache:          null        # Project cache (symfony type only)
        logs:           null        # Project logs  (symfony type only)
        proxy:                      # Proxy configuration (proxy type only)
          port:      null               # Proxy port (required)
          adress:    "http://127.0.0.1" # Proxy adress (optional)
          websocket: false              # WebSocket handshake support (optional)


Example Playbook
----------------

    - hosts: servers
      vars:
        elao_projects:
          -
            { name: foo, type: symfony, host: foo.dev }
            { name: bar, type: silex, host: bar.dev }
      roles:
         - { role: elao.projects }


License
-------

MIT


Author Information
------------------

http://www.elao.com/
