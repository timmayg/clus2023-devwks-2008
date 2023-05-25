# Configure MACsec PSK on VLAN Trunk Link

MACsec enables wire speed AES encryption. This wire speed encryption comes with 
all Catalyst 9000 switches. MACsec is the protocol that performs the bulk data
encryption. MACsec requires MKA (MACsec Key Agreement). MKA is the process that
is used for key generation and key exchange. 

Refer back to our network diagram and see that our Cat9300 switches are connected
to each other via GigabitEthernet1/0/1. 

In this example we create the necessary MKA configuration, MKA policy to enable
AES-256 encryption, and enable MACsec on the switchports.  Configuring MACsec PSK
is fairly simple for such a powerful encryption method. 

MACsec can also use Certificates instead of PSK, we wont do that today. :-)  


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
