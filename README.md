# Ansible_Project-

Ansible is a configuration tool used to configure and manage multiple nodes at a single time

### Configuring Ansible

To configure ansible you need some linux machines. In this project I used VMWare to create multiple Linux machines and used Redhat Linux as a OS 

after the installaion ......... of all os select a machine for client and other for managed nodes

#### step: 01
firstly install ansible pckg on selected server machine 

    sudo yum install ansible* -y

some times ansible required epel ( extra packages for enterprises Linux ) 

Ansible is agent less so there is no need to configure ansible on oher sides ansible use ssh portocol to give command
Write down the all ip addressed of every node and create a ssh connection 

    sudo ssh 
