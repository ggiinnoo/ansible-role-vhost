Domain setup
=========

Setup domain names.

For presta shop, only nginx is available!

Requirements
------------

webserver

Role Variables
--------------

Not yet explained

Dependencies
------------

None

Example Playbook
----------------

    ---
    - name: setup domain names
      hosts: groupWeb
      roles:
       - domainSetup

License
-------

BSD

Author Information
------------------

Creator: Gino Jansen
Website: www.ginojansen.nl