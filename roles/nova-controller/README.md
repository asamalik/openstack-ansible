Role Name
=========

A brief description of the role goes here.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| mysql_root_password | redhat | Root password for the Mari- aDB database. |
| controller_hostname | controller | Hostname of the controller node. |
| keystone_admin_token | keystone_admin_token | Admin token for the Open- Stack Keystone service. |
| nova_db_password | redhat | Database password for the OpenStack Compute service. |
| nova_password | redhat | Keystone password for the OpenStack Compute service. |
| rabbit_password | redhat | Password for the AMQP mes- sage bus. |
| controller_ip | 10.0.0.11 | IP address on the interface attached to the Management network. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
