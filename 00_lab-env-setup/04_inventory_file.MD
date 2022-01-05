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
       -  Default location >> /etc/ansible/hosts file 
       -  Using -i option >> ansible -i my_hosts

