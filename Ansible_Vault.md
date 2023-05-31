# Ansible Vault Usage

It's great to see you checking out other topics! I hope you have made it through all four of the labs. 

You will have seen our playbooks point to an Ansible Vault file. This is the code that is used in the playbooks. 

<code> vars_files:
  - ~/clus2023-devwks-2008/vaults/ciscolive.vault</code> 

What does this do? 
<br>
What does this mean?

vars_files tells the ansible playbook that it should look to the files listed for variables. The variables can be encrypted or they can be in the clear. Ansible doesnt care.  

<ol>

<li>Assure No Cleartext Passwords Exist </li>
<br>
In this step we will check the inventory files to assure that they do not contain the IOS XE Username and password in the clear. We will check all 3 inventory files. 
<br><br>
<code>cat inventories/cat9300-a.yaml</code>
<br><br>
<code>cat inventories/cat9300-b.yaml</code>
<br><br>
<code>cat inventories/devnet-switches.yaml</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>View the Playbook </li>
<br>
Now we know the Username and Password doesnt exist in the clear. Next we will cat the playbook and find the vars_files line that points to the Ansible Vault file that contains the encrypted Username and Password. 
<br>
<code>cat playbooks/01b-config-hard-https.yaml</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>Assure the Ansible Vault File Exists </li>
<br>
Lets just verify there is a file with the correct name. 
<br>
<code>ls -l vaults/ciscolive.vault</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>View the Encrypted File </li>
<br>
Please note the top line.  This header shows us this is an Ansible Vault file. It is using Ansible Vault encryption version 1.1.  It shows the file is encrypted using AES256. Finally it shows the encrypted variables. 
<br>
<code>cat vaults/ciscolive.vault</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>View the Encrypted File's Contents in Cleartext </li>
<br>
In this step we will decrypt the contents on the fly for viewing. Be aware, if you log the contents of your SSH session you will log the clear text password!!!  
<br>
<code>ansible-vault view vaults/ciscolive.vault</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

</ol>

## [Main Page](/README.md)


