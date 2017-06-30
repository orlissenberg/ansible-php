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

      roles:
        - ansible-php

License
-------

MIT

Additional Information
----------------------

DOTDEB no longer does PHP releases, now use:

Ondřej Surý also provides PHP 7.1 packages for Debian

[Installing PHP 7.1](https://www.colinodell.com/blog/2016-12/installing-php-7-1)

[Nginx PHP via FastCGI](http://wiki.nginx.org/Configuration#PHP_via_FastCGI)

Check composer

    composer diagnose

Check the PHP modules

    php -m

Serve a Laravel project without a web server

    php artisan serve --host 0.0.0.0 --port 8080

In the event of failure:

    sudo apt-get purge php7.0 php7.0-cli php7.0-fpm -y
    sudo rm -Rf /etc/php/fpm; sudo rm -Rf /etc/php/cli;
    sudo systemctl status php7.0-fpm.service

Copy from a fresh installation:

    ﻿sudo cp /etc/php/7.0/fpm/php-fpm.conf /vagrant/ansible/roles/ansible-php/templates/php7-fpm.conf.j2
    ﻿sudo cp /etc/php/7.0/fpm/php.ini /vagrant/ansible/roles/ansible-php/templates/php7-fpm.ini.j2
