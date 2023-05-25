# Configure IOS XE to use Type 6 Password Encryption where Applicable

In 2023, Type 5 and Type 7 passwords should never be used. Type 6 passwords are
stored after being encrypted with AES-128. 

Type 6 passwords are typically used for RADIUS & TACACS shared secrets, & IPSec 
and MACsec pre-shared-keys. Type 6 is encryption, not hashing like Type 8 & 9. 
Type 6 uses encryption because the passwords need to be decrypted so that IOS
processes can use them, eg, using an IPSec PSK to encrypt data before sending it
over the wire. 


<ol>

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
