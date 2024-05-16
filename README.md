# Ansible_Project-

Ansible is a configuration tool used to configure and manage multiple nodes at a single time

### Configuring Ansible

To configure ansible you need some linux machines. In this project I used VMWare to create multiple Linux machines and used Redhat Linux as a OS 

after the installaion ......... of all os select a machine for client and other for managed nodes

#### Step: 01
Create a user on every system and give them sudo permisiions 

to give the sudo perminssion for any user go to sudoers file and add the line above root user line  

    user    ALL=(ALL)    NOPASSWD:ALL

#### Step: 02       
firstly install ansible pckg on selected server machine 

    sudo yum install ansible* -y

some times ansible required epel ( extra packages for enterprises Linux ) 

#### Step: 03
Active and enable SSH on all systems 

    sudo systemctl start ssh

#### Step: 04
On the server create a ssh key 

    sudo ssh key-gen
    
#### Step: 05
NoW copy this key into every system using ssh protocol

    sudo ssh copy-id 

#### Step: 06
Add ip of client machine in the inventory file and run a ansible adhoc command to check the conectivity of the systems 

    sudo ansible all -m ping
