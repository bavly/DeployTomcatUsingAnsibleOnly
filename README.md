# Task-deployapplication

## Running Playbook

Once all values are updated, you can then run the playbook against your nodes.

Just crate hosts file 

- Update your inventory, e.g:

```
$ vim hosts
[tomcat-nodes]
172.161.1.1       # Remote user to act on
```
Playbook executed as root user - with ssh key:

```
$ vim startTomcat&helloWorld
- name: Tomcat deployment playbook & deployment
  hosts: tomcat-nodes    
  become: yes             
  roles:
    - tomcat
```
$ ansible-playbook -i hosts startTomcat&helloWorld.yml
```

## Do not forget to open ssh connection between target servers & ansible 
