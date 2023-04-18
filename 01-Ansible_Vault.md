# Ansible Vault

In this section we will work with Ansible Vault. 
Storing Username and Passwords in your Inventory or Playbooks needs to be a thing of the past. 

<ol>
<li>View the Unencrypted User & Password file.</li>
![Unencrypted User\Password File](/images/01-01-cat-authc-vault.png)

```cat vaults/authc.vault```  

<li>Encrypt the variable file.</li>
Use the password cisco123 

```ansible-vault encrypt authc.vault```  
    
<li>View the encrypted variable file.</li>

```cat authc.vault```  
    
<li>Use Ansible Vault to view the encrypted variable file.</li>
Remember, the password is cisco123

```ansible-vault view authc.vault```  
   

</ol>  
