# Ansible Vault

In this section we will work with Ansible Vault. 
Storing Username and Passwords in your Inventory or Playbooks needs to be a thing of the past. 

<ol>

<li>Change directory to the Ansible root directory.</li>
<code>cd /etc/ansible</code>
<br><br><br>

<li>View the Unencrypted User & Password file. </li>  
ansible_user & ansible_password are variables. The variables contain the username and password that will be used to authenticate to the Cat9K switch. In this case we will only encrypt these varibles, but you should understand that Ansible Vault can be used to encrypt ANY variable.     
<br>
<code>cat vaults/authc.vault</code>
<br><br>
<img src="/images/01-01-cat-authc-vault-web.png" alt="Unencrypted User\Password File" width=600>
<br><br><br>

<li>Encrypt the variable file, use the password <b>abcd9876</b> </li>
Use this command to encrypt the file that contains the variables.  
Assure the encryption password is entered correctly and that the the Encryption successful message is displayed.
<br>
<code>ansible-vault encrypt vaults/authc.vault</code>
<br><br>
<img src="/images/01-02-ansible-vault-encrypt-web.png" alt="Ansible Vault Encryption Process" width=600>    
<br><br><br>

<li>View the encrypted variable file.</li>
The top line identifies the file as an Ansible Vault File. The file is encrypted using Ansible Vault version 1.1. The encryption algorithm is 256-bit AES.
<br>
<code>cat vaults/authc.vault</code>
<br><br>
<img src="/images/01-03-cat-authc-vault-encry-web.png" alt="Encrypted User\Password File" width=600>
<br><br><br>

<li>Use Ansible Vault to view the encrypted variable file.</li>
Remember, the password is <b>abcd9876</b>
<br>
<code>ansible-vault view authc.vault</code>
<br><br>
<img src="/images/01-04-ansible-vault-view-web.png" alt="Using Ansible-Vault View to See Unencrypted Variables" width=600>
<br><br><br>
</ol>  

<li>Observe the contents of the Inventory File </li>
<br>
<code>cat inventories/devnet-switches.yaml</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

[Click here to Move on to the next section. Working with SSH Keys. ](/02-SSH_Keys.md)


