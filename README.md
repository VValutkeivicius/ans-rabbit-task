1. Clone repo to Ansible master
2. In hosts file please update
 a. the entry ```ansible_ssh_private_key_file= ``` with the location to the auth certificate for the server the playbook will have to run on
 b. Under servers ``` HOST_ADDR ``` for the address of the server
 c. Entry ``` ansible_user= ``` with the user name
3. Run bellow command
```
 ansible-playbook -b main.yml --ask-vault-pass
```
When prompted for ansible-vault password it was provided in the email.

Sorry don't think I accomplished the the parts with the firewall and the publisher script. The publisher is added but I think it won't work since the docket container is not on the same internal network as RabbitMQ. 