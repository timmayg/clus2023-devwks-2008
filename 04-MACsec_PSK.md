# Configure MACsec PSK on VLAN Trunk Link

MACsec enables wire-speed AES encryption. This wire-speed encryption comes with all Catalyst 9000 switches. MACsec is the protocol that performs bulk data encryption. MACsec requires MKA (MACsec Key Agreement). MKA is the process that is used for key generation and key exchange. 

Refer to our network diagram and see that our Cat9300 switches are connected via GigabitEthernet1/0/1. 
[Network Diagram](/labs-pods.md)

In this example we create the necessary MKA configuration, MKA policy to enable
AES-256 encryption, and enable MACsec on the switchports.  Configuring MACsec PSK
is fairly simple for such a powerful encryption method. 

MACsec can also use Certificates instead of PSK, but we aren't going to do that
today. :-)  


<ol>

<li>View the MACsec Playbook using cat </li>
You will notice that this is a very long playbook with several tasks. Because all of these tasks are configured with NETCONF RPCs, putting them all into the same playbook is the most efficient. So now we will look at each of the RPCs in detail below. 
<br>
<code>cat playbooks/04-config-macsec-psk.yaml</code>
<br><br>
This task will shutdown the interface. When making changes like this the interface
should be shutdown. 
<img src="/images/04-01-cat-shutdown-web.png" alt="" width=600>
<br><br>
This task will configure the MKA Keys, which will be attached to the interface later. The MKA Keys consist of a CKN (Connectivity Key Name) and a CAK (Connectivity Association Key). The CAK is the root of all other keys, including the SAK (Security Association Key), the actual key that does bulk data encryption.
<img src="/images/04-02-cat-ckn-cak-web.png" alt="" width=600>
<br><br>
<img src="/images/04-03-cat-mka-policy-web.png" alt="" width=600>
<br><br>
<img src="/images/04-04-cat-interface-description-web.png" alt="" width=600>
<br><br>
<img src="/images/04-05-cat-int-mka-pol-web.png" alt="" width=600>
<br><br>
<img src="/images/04-06-cat-int-mka-key-web.png" alt="" width=600>
<br><br>
<img src="/images/04-07-cat-int-macsec-network-link-web.png" alt="" width=600>
<br><br>
<img src="/images/04-08-cat-no-shutdown-web.png" alt="" width=600>

<br>


<li>Run the Playbook </li>
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/04-config-macsec-psk.yaml --ask-vault-pass
</code>
<br><br>
<img src="/images/04-09-playbook-output-macsec-web.png" alt="" width=600>
<br><br><br>


<li>Check the MKA Status on the Switch </li>
<br>
<code>show mka session</code>
<br><br>
<img src="/images/04-10-show-mka-status-web.png" alt="" width=600>
<br><br><br>


<li>Check the MACsec Status on the Switch </li>
<br>
<code>show macsec summary</code>
<br><br>
<img src="/images/04-11-show-macsec-summary-web.png" alt="" width=600>
<br><br><br>



</ol>
