# learning_ansible

This is a small repo for the playbooks I will be making while going through the [Getting Started with Ansible](https://www.youtube.com/playlist?list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70) playlist made by LearnLinuxTV on YouTube. 

# description

For the first portion of this repository, I have deployed five virtual machines using VMWare. The inventory at this stage is:
- 2 web servers (Ubuntu, CentOS)
- 1 database server (Ubuntu)
- 1 file server (Ubuntu)
- 1 workstation (Ubuntu)

The purpose of having two different web servers is to demonstate and practice separate requirements for each operating system. 

## playbooks

### current

bootstrap.yml: simple bootstrap to get the OS updated and a test user installed on a newly deployed server

site.yml: ensures servers have most current repository index, runs plays by host and role

### to be cleaned/retired

install_apache.yml: simple playbook used to install apache package to server, now redundant

remove_apache.yml: simple playbook used to remove apache package from server, may either be refactored or retired.

site_before_roles.yml: backup of site.yml before refactoring and reorganizing for easier administration using roles, variables, and handlers.

## roadmap

- refactor or remove baseline.yml, general repo cleanup
- playbook for establishing the baseline security configuration of web server
- playbook for establishing the baseline security configuration of database server
- playbook for establishing the baseline security configuration of file server
- playbook for establishing the baseline security configuration of workstations

