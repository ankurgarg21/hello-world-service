# hello-world-service
hello-world-service project 

Scripts to automate build infra stack tasks

## By Vagrant
Vagrantfile includes config to bulid spring boot app stack with following packages
Java
Maven
Jenkins 

# Commands
vagrant up
vagrant provision

Make sure ansible is installed on your host

## Ansible playbooks

# Include config to install infra stack for spring boot app
$ ansible-playbook -i hosts -v playbook.yml 

#include config to deploy spring boot app
$ ansible-playbook -i hosts -v deploy.yml



