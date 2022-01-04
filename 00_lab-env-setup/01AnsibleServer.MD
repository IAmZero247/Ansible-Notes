# Ansible Server 

 1. Setup EC2 instance
 2. Setup Hostname
 3. Create ansibleadminuser
 4. Add user to sudoens file
 5. Generate ssh key
 6. Enable password based login
 7. Install Ansible
 
 
 ## Setup EC2 
    
    ```
    1. use amazon linux ami
    2. new security group -> ansible-sg
           `open port`  `22`
                        `80`
                        `8080`
    ```
