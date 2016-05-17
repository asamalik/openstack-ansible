Role Name
=========

The role neutron-controller installs the controller services of the OpenStack Networking service.


Role Variables
--------------

| Variable Name | Default Value | Description
| --- | --- | --- |
| mysql_root_password | redhat | Root password for the Mari- aDB database. |
| controller_hostname | controller | Hostname of the controller node. |
| keystone_admin_token | keystone_admin_token | Admin token for the Open- Stack Keystone service. |
| neutron_db_password | redhat | Database password for the OpenStack Networking ser- vice. |
| neutron_password | redhat | Keystone password for the OpenStack Networking ser- vice. |
| nova_password | redhat | Keystone password for the OpenStack Compute service. |
| management_interface_name | eth1 | Name of the interface at- tached to the Management network. |
| public_interface_name | eth2 | Name of the interface at- tached to the VM network. |
| overlay_interface_ip | 10.0.0.11 | IP address on the interface attached to the Management network. |
| metadata_secret | metadata_secret | A secret for the metadata agent. |
| rabbit_password | redhat | Password for the AMQP mes- sage bus. |


License
-------

GPLv3


Other Information
-----------------

This role has been created by Adam Samalik as a part of his Bachelor's thesis.
Code lives on: https://github.com/asamalik/openstack-ansible
