# AD HOC COMMANDS

  - https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html

### Syntax 

  ```
  $ ansible [pattern] -m [module] -a "[module options]"
  ```
  
  1. `Examples of modules` 
      
      -  ping >>
         ```
            ansible all -m ping
         ```   
      -  command >>
         ```
         ansible all -m command -a "uptime"
         ansible all -m command -a "date"
         ansible all -m command -a "who"
         ansible all -m command -a "whoami"
         ansible all -m command -a "pwd"
         ```
      -  stat >>
         ```
           ansible all -m stat -a "path=/etc/hosts"
         ```
      -  yum >>
      -  user >>
      -  setup >>
