Role Name
=========

The role cinder-controller installs the controller services of the OpenStack Block Storage service.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| controller_hostname | controller | Hostname of the controller node. |
| mysql_root_password | redhat | Root password for the Mari- aDB database. |
| controller_ip | 10.0.0.11 | IP address on the interface attached to the Management network. |
| cinder_password | redhat | Keystone password for the OpenStack Block Storage service |
| cinder_db_password | redhat | Database password for the OpenStack Block Storage service |
| rabbit_password | redhat | Password for the AMQP message bus. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
