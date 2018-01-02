# Maven ansible role


[![Build Status](https://travis-ci.org/tecris/ansible-maven.svg?branch=master)](https://travis-ci.org/tecris/ansible-maven)


Role Variables
--------------

[defaults/main.yml](defaults/main.yml)

|*Variable*  | *Default Value* |*Description* |
| --- | --- | --- |
| maven_major | 3 | MAJOR [version](http://semver.org/) |
| maven_version | 3.5.0 | Version number|
| maven_home_parent_directory | /opt | MAVEN_HOME parent directory|

Installation
------------

 `$ ansible-galaxy install tecris.maven`

Example Playbook
----------------
```
 - hosts: all
   roles:
     - { role: tecris.maven, maven_major: 3, maven_release: 3.5.0, maven_home_parent_directory: /opt }
```
Tests
-----
References:
 - [Ansible role testing](http://www.jeffgeerling.com/blog/testing-ansible-roles-travis-ci-github)
 - [Ansible apache role](https://github.com/geerlingguy/ansible-role-apache)
