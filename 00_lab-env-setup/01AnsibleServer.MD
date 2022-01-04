# Ansible Server 

 1. Setup EC2 instance
 2. Setup Hostname
 3. Create ansibleadmin user
 4. Add user to sudoens file
 5. Generate ssh key
 6. Enable password based login
 7. Install Ansible
 
 
 
 
 ### Setup EC2 
    
      
- use amazon linux ami
- new security group -> ansible-sg
                open port  22
                           80
                           8080
                           
 ### Setup Hostname
    
- Hostname command
      
   ```sh
		sudo su - 
		hostname ans-control-node
   ``` 
    
- Edit /etc/hostname
    
  ```
        vi /etc/hostname
        ans-control-node
        
        sudo su -
  ```

 ### Create ansibleadmin user
 
   ```sh
		useradd ansibleadmin
		passwd  ansible12345
   ```
 
 ### Add user to sudoens file
   
   ```sh
      
	   visudo 
	   
	   add under root
	   
	   `ansibleadmin ALL=(ALL)	NOPASSWD:ALL `
   
   ```