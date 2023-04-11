# Cisco Live US 2023
# DEVWKS-2008 - Reducing the Attack Surface of IOS XE with Ansible

## Ansible Vault

1. View the Unencrypted User & Password file.

    cat userpass

2. Encrypt the variable file. 
Use the password cisco123 

    ansible-vault encrypt userpass
    
3. View the encrypted variable file

    cat userpass
    
4. Use Ansible Vault to view the encrypted variable file. 
Remember, the password is cisco123

    ansible-vault view userpass
  
5.   
  
  
  
  
  
  
