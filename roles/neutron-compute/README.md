Role Name
=========

The role neutron-compute installs the compute services of the OpenStack Networking service.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| controller_hostname | controller | Hostname of the controller node. |
| rabbit_password | redhat | Password for the AMQP mes- sage bus. |
| neutron_password | redhat | Keystone password for the OpenStack Networking ser- vice. |
| public_interface_name | eth2 | Name of the interface at- tached to the VM network. |
| overlay_interface_ip | 10.0.0.31 | IP address on the interface attached to the Management network. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
