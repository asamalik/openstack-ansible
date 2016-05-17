Role keystone
=========

The role keystone installs the OpenStack Identity service.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| mysql_root_password | redhat | Root password for the MariaDB database. |
| keystone_db_password | redhat | Database password for the OpenStack Keystone service. |
| keystone_admin_token | keystone_admin_token | Admin token for the OpenStack Keystone service. |
| controller_hostname | controller | Hostname of the controller node. |
| admin_password | redhat | Password for the default admin user. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
