# Cisco Live US 2023
# DEVWKS-2008 - Reducing the Attack Surface of IOS XE with Ansible

## Ansible Vault Section




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
  
  
  
  
  
  
