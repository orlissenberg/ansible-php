Ansible PHP
==========

Install PHP

Requirements
------------

Debian.

Role Variables
--------------

...

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - hosts: webservers
      gather_facts: yes
      sudo: yes

      roles:
        - ansible-php

License
-------

MIT

Additional Information
------------------

[Nginx PHP via FastCGI](http://wiki.nginx.org/Configuration#PHP_via_FastCGI)

Check composer

    composer diagnose

Check the PHP modules

    php -m

Serve a Laravel project without a web server

    php artisan serve --host 0.0.0.0 --port 8080
