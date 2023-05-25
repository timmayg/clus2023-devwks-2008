# Configure IOS XE to use Type 6 Password Encryption where Applicable

In 2023, Type 0 (cleartext) Type 5 (Md5 Hashed) and Type 7 (obfuscated) 
passwords should never be used. Type 6 passwords are stored after being 
encrypted with AES-128. 

Type 6 passwords are typically used for RADIUS & TACACS shared secrets, & IPSec 
and MACsec pre-shared-keys. Type 6 is encryption, not hashing like Type 8 & 9. 
Type 6 uses encryption because the passwords need to be decrypted so that IOS
processes can use them, eg, using an IPSec PSK to encrypt data before sending it
over the wire. 


<ol>

<li>View the Playbook that will enable Type 6 password storage </li>
This playbook contains two commands.  These two commands will configure a master key which will then be used to encrypt any passwords which will use Type 6 encryption. 
<br>
<code>cat playbooks/03-config-type6.yaml</code>
<br><br>
<img src="/images/03-01-cat-type6-web.png" alt="" width=600>
<br><br><br>


<li>Run the Playbook </li>
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/03-config-type6.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li> </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li> </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

</ol>

[Click here to move on to the next section. Configuring Switch to Switch MACsec Encryption. ](/04-MACsec_PSK.md)