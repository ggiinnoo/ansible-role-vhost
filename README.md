Domain setup
=========

Setup domain names.

For presta shop, only nginx is available!

Requirements
------------

webserver

Role Variables
--------------

The variable "web_server: "" Needs to be set in the inventory file."

    # Ignore vhost staging error's
    ignore_vhost_errors: true

This variable can be used to ignore errors on staging domain's

Custom vhosts can be set for both nginx or httpd with the following variables in the inventory file:
    
    # httpd vhost xcart site
    httpd_vhost_xcart: "{{playbook_dir}}/templates/<customfile>.j2"
    
    # httpd vhost magento site
    httpd_vhost_magento: "{{playbook_dir}}/templates/<customfile>.j2"
    
    # httpd vhost symfony style
    httpd_vhost_symfony: "{{playbook_dir}}/templates/<customfile>.j2"
    
    # nginx vhost xcart site
    nginx_vhost_xcart: "{{playbook_dir}}/templates/<customfile>.j2"
    
    # nginx vhost magento site
    nginx_vhost_magento: "{{playbook_dir}}/templates/<customfile>.j2"
    
    # nginx vhost symfony style
    nginx_vhost_symfony: "{{playbook_dir}}/templates/<customfile>.j2"

The following web systems work:

    xcart
    symfony
    oro
    magento
    presta (nginx only)

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