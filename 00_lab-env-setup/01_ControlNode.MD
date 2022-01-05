# Ansible Server - Control Node

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
    
- Edit /etc/hostname [Permanent]
    
   ```sh
        vi /etc/hostname
        ans-control-node
        
        sudo su -
   ```

 ### Create ansibleadmin user
 
   ```sh
		useradd ansadmin
		passwd  ans12345
   ```
 
 ### Add user to sudoens file
   
   ```sh
      
	   visudo 
	   
	   add under root
	   
	   `ansadmin ALL=(ALL)	NOPASSWD:ALL `
   
   ```
   
 ### Generate ssh key
   
   ```sh
     
     sudo su - ansadmin 
	
     #generate sshkey with empty passphrase
	
     ssh-keygen
     ll -a
	
     cd .ssh
	
       >> 1. id_rsa
       >> 2. id_rsa.pub
	
   ```
    
### Enable password based login   


  ```
      switch to root 
    
      sudo su - 
      whoami
    
      vi /etc/ssh/sshd_config
    
      now update for below:
      PasswordAuthentication yes
    
      service sshd restart | reboot
   ```
 
 ### Install Ansible
 
   1. Install python and python-pip
   
   ```sh
       yum install python
       yum install python-pip
   ```
   
   2. Install ansible using pip check for version
     
   ```sh
     
      pip install ansible
      ansible --version
     
    ```
    
