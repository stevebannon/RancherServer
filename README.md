# RancherServer
Using Ansible to set up Rancher server and register hosts

This is a trimmed down version of Hussein Galal's fine rancher-ansible example
https://github.com/galal-hussein/Rancher-Ansible


CONFIGURE THE INSTALL
=========
hosts needs to be updated with the addresses of the machines that will be serving each role

the docker user needs to be updated in rols/docker/defaults/main.yml

ansible will need a user on each host for ssh access
   - same username on all hosts (inour case, elsa)
   - public ssh key should be installed
   - will need passwordless sudo if not root

RUN THE PLAYBOOK
==========

ansible-playbook -u elsa -i hosts --sudo rancher.yml

