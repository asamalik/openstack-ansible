Role Name
=========

The role cinder-storage installs the storage services of the OpenStack Block Storage
service.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| controller_hostname | controller | Hostname of the controller node. |
| cinder_db_password | redhat | Database password for the OpenStack Block Storage service |
| rabbit_password | redhat | Password for the AMQP message bus. |
| cinder_password | redhat | Keystone password for the OpenStack Block Storage service |
| management_ip | 10.0.0.41 | IP address on the interface attached to the Management network. |
| cinder_volume_group | cinder-volumes | Name of the volume group used by the OpenStack Block Storage service. |
| cinder_partition | /dev/sdb | Partition used by the Open- Stack Block Storage service. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
