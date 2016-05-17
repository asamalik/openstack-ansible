# Ansible Roles to Deploy OpenStack

This repository contains Ansible roles to deploy basic OpenStack cloud. They can be modified and reused to deploy more complex environments.

These roles have been developed as part of my [Bachelor's thesis](https://github.com/asamalik/bc-thesis/blob/master/projekt.pdf).


**Important: NEVER use this deployment in production without modifications. All passwords are saved in plain text in this repository.** It is up to the user to modify the configuration accordingly.

## Testing environment

To test the roles easily, I have included a Vagrantfile that provisions the virtual machines for you.

You can run the deployment by:

```
$ vagrant up
$ ansible-playbook deploy-openstack.yml
```

The configuration has been tested on MacOS X with VirtualBox. You will also need to have Vagrant and Ansible version 2 installed on your system.

You will be able to access the OpenStack Dashboard on [http://10.0.0.11/dashboard](http://10.0.0.11/dashboard) if you use the default configuration. 

Log in using:
* Domain: default
* User: admin
* Password: redhat


## Licensing

The roles themselves are licensed under GPL Version 3 license. There are also some Ansible Modules created by Davide Guerri that are licensed under Apache Version 2.0 license.
