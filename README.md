# Delivery service
This repo contains an [Ansible](http://www.ansible.com/) role to deploy a delivery service consinsting 
of a WebDAV server (Apache2 enabled) and an FTPES server (Proftpd enabled).  
Both servers use the same data path and users can retrieve data indifferently
 from the WebDAV or FTPES server.  
 All the communications are encrypted using SSL enabled data channel.
  
## Requirements
This role requires Ansible 2.0+. See [Ansible installation](http://docs.ansible.com/ansible/intro_installation.html)

## Variables
In _vars/main.yml_, you will find all the variables that the role is using.  
Configure them accordingly to your setup.


## Usage
Digit:  
```bash
ansible-playbook -i inventory setup_server.yml
```
to setup the servers on your remote host defined into the inventory file


Digit: 
```bash
ansible-playbook -i inventory create_user
```
to create a user with a random username and a random generated password.  
This user can be used to log in into the WebDAV and the FTPES servers.