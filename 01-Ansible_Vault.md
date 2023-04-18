# Ansible Vault

In this section we will work with Ansible Vault. 
Storing Username and Passwords in your Inventory or Playbooks needs to be a thing of the past. 

<ol>
<li>View the Unencrypted User & Password file. </li>  

ansible_user & ansible_password are variables that point to username and password that will be used to login to the Catalyst 9000.  
  
In this case we are only going to encrypt these varibles, but please understand that you are able to encrypt ANY variable that you would like.     

```cat vaults/authc.vault```  

<img src="/images/01-01-cat-authc-vault.png" alt="Unencrypted User\Password File" width=600>
$~$
$~$
<li>Encrypt the variable file, use the password cisco123 </li>
Use this command to encrypt the file that contains the variables.  
  
```ansible-vault encrypt vaults/authc.vault```  

<img src="/images/01-02-ansible-vault-encrypt.png" alt="Ansible Vault Encryption Process" width=600>    
<li>View the encrypted variable file.</li>
256-bit AES with salt is used to encrypt the file.

```cat authc.vault```  

<img src="/images/" alt="" width=600>


<li>Use Ansible Vault to view the encrypted variable file.</li>
Remember, the password is cisco123

```ansible-vault view authc.vault```  

<img src="/images/" alt="" width=600>


</ol>  
