Role Name
=========

The role sql-database installs the MariaDB database.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| mysql_root_password | redhat | Root password for the Mari- aDB database. |
| controller_hostname | controller | Hostname of the controller node. |
| controller_management_ip | 10.0.0.11 | IP address on the interface attached to the Management network. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
