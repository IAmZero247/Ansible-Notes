# Inventory File 

  - https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html

### Sample File in Default Location /etc/ansible/hosts
  ```
      cat /etc/ansible/hosts

      [rhel]
      host1 
      host2
      [ubuntu]
      host3
      host4
      [other]
      host5
  ```
  
  ### Host Info 
  
  1. Setup EC2 instance
  2. Setup Hostname
  3. Create ansibleadmin user
  
  1.  Default location >> /etc/ansible/hosts file 
  2.  Using -i option >> ansible -i my_hosts
  3.  Define in ansible.cfg file 

