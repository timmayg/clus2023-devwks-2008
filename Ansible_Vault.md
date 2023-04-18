#Ansible Vault

In this section we will work with Ansible Vault. 
Storing Username and Passwords in your Inventory or Playbooks needs to be a thing of the past. 

1. View the Unencrypted User & Password file.

```cat authc.vault```

2. Encrypt the variable file. 
Use the password cisco123 

```ansible-vault encrypt authc.vault```
    
3. View the encrypted variable file

```cat authc.vault```
    
4. Use Ansible Vault to view the encrypted variable file. 
Remember, the password is cisco123

```ansible-vault view authc.vault```
  
5.   
  
