# ANSIBLE CONFIG FILE | ansible.cfg 

-  https://docs.ansible.com/ansible/latest/reference_appendices/config.html

### Precedence 
-  Changes can be made and used in a configuration file which will be searched for in the following order:

1. ANSIBLE_CONFIG (environment variable if set)

1. ansible.cfg (in the current directory)

1. ~/.ansible.cfg (in the home directory)

1. /etc/ansible/ansible.cfg

  Ansible will process the above list and use the first file found, all others are ignored
