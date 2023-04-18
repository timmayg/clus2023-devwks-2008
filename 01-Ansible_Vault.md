# Ansible Vault

In this section we will work with Ansible Vault. 
Storing Username and Passwords in your Inventory or Playbooks needs to be a thing of the past. 

<ol>
<li>View the Unencrypted User & Password file. </li>  
ansible_user & ansible_password are variables that point to username and password that will be used to login to the Catalyst 9000. 

```cat vaults/authc.vault```  

![Unencrypted User\Password File](/images/01-01-cat-authc-vault.png)


<li>Encrypt the variable file.</li>
Use the password cisco123 

```ansible-vault encrypt authc.vault```  
    
<li>View the encrypted variable file.</li>

```cat authc.vault```  
    
<li>Use Ansible Vault to view the encrypted variable file.</li>
Remember, the password is cisco123

```ansible-vault view authc.vault```  
   

</ol>  
