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
- vagrant ssh

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

## Install Jenkins job Builder in your server
$ sudo pip install jenkins-job-builder
 
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


# Jenkins Configuration 
- Make sure all required plugins installed
- Configure github webhook for push event 

# Test Job
- A Job testing has been created to get push event on pull request on master branch 

# Deploy Job
- Deploy job has been created once pull request merge to master then can be deployed on server 

# Current Settings
All current settings has been confgured to test only on localhost using below tools and technologies
App is currently not configured to run as a background service 

- ubuntu/xenial64
- Java
- Maven
- Jenkins
- Ansible
- Vagrant 
- Jenkins Job Builder
- Github

# Version Deploy App
- Can use tag based release in stage envoirnment to deploy with latest tag only
- Can use master branch only to deploy in production once PR merged to master

## Thanks 
 

