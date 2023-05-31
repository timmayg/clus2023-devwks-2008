# Configure IOS XE to use Type 6 Password Encryption where Applicable

It's 2023, Type 0 (cleartext) Type 5 (MD5 Hashed) and Type 7 (obfuscated) passwords should never be used. In this exercise, we will enable Type 6 password encryption. Type 6 passwords are securely stored after being encrypted with AES-128. 

Type 6 passwords are typically used for RADIUS & TACACS shared secrets, & IPSec and MACsec pre-shared keys. Type 6 is encryption, not hashing like Type 8 & 9. Type 6 uses encryption because these passwords need to be decrypted so that IOS processes can use them, e.g., using an IPSec PSK to encrypt data before sending it over the wire. 


<ol>

<li>View the Playbook that will enable Type 6 password storage. </li>
<br>
This playbook contains two commands.  These two commands will configure a master key which will be used to encrypt any passwords to use Type 6 encryption. 
<br>
<code>cat playbooks/03-config-type6.yaml</code>
<br><br>
<img src="/images/03-01-cat-type6-web.png" alt="" width=600>
<br><br><br>


<li>Run the Playbook </li>
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/03-config-type6.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/03-02-playbook-output-type6-web.png" alt="" width=600>
<br><br><br>

Excellent!   
Type 6 passwords have been enabled. Currently, no Type 6 password 
exists on our IOS XE boxes, but in the next task, we will create some key chains containing pre-shared keys; those are stored in Type 6 format! Let's go!!!


</ol>

[Click here to move on to the next section. Configuring Switch to Switch MACsec Encryption. ](/04-MACsec_PSK.md)