# hello-world-service
hello-world-service project

# Clone the repo
https://github.com/ankurgarg21/hello-world-service.git

# Change directory 
$ cd hello-world-service  

# Scripts to automate build infra stack tasks

# By Vagrant
Vagrantfile includes config to bulid spring boot app stack with following packages

- Java
- Maven
- Jenkins 

# Commands
- vagrant up
- vagrant provision

Make sure ansible is installed on your host

## Ansible playbooks

# Using Ansible Version 
ansible 2.4.2.0

# Include config to install infra stack for spring boot app
$ ansible-playbook -i hosts -v playbook.yml 

Jenkins will listen on port localhost:8082

# include config to deploy spring boot app
$ ansible-playbook -i hosts -v deploy.yml

# App Path: /opt/hello-world/
App will listen on port localhost:8080


# Automate Jenkins Jobs

To automate jenkins jobs using Jenkins Job Builder

## Jenkins jobs
Create a jenkins job ini-file

```
[jenkins]
url=http://localhost:8082/
user=youruser
password=password
```

# Command to build jenkins jobs

$ jenkins-jobs --conf ankur.ini update jenkins-job/




