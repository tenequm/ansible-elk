Ansible Role: ELK
=========

A role for ELK stack installation on Nginx server. Watch out that it was supposed to be used for the newly created machines, so using it over some existing can cause damage to it. Also it establishes SSL certificates and connects them to Nginx server.

Role Variables
--------------
*REQUIRED VARIABLES*
`elk_server_domain: ''` - domain name of the server you're going to provide it on, as it will also establish automated SSL certificates from Letsencrypt.

*OTHER VARIABLE*
`elk_ssl_email: ''` - email which your certificates will be registered to.
`elk_kibana_users: []` - list of users who will have access to Kibana panel.

Dependencies
------------

It dependence on `tenequm.nginx` role, so be sure you have it installed before running this role.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: tenequm.elk, elk_server_domain: "example.com" }

License
-------

MIT

Author Information
------------------

This role was created in 2017 by [Mykhaylo Kolesnik](http://github.com/1nfinitum).
