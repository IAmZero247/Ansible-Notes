# AD HOC COMMANDS

  - https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html

### Syntax 

  ```
  $ ansible [pattern] -m [module] -a "[module options]"
  ```
  
  1. Examples of modules 
    -  ping
       `ansible all -m ping`
    -  command
       `ansible all -m command -a "uptime"`
    -  Stat
    -  yum
    -  user
    -  setup
