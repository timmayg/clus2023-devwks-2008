# Harden IOS XE SSH & HTTPS Services

Now it's time to run some Ansible Playbooks and Reduce the Attack Surface of the IOS XE box! <br>

The SSH server on IOS XE supports several cryptographic primitives for compatibility reasons. As security-minded network engineers, we must recognize that some are less secure than others. In this task, we will run a playbook that will modify the SSH server to only use highly secure cryptographic primitives. Modern versions of the popular SSH clients (e.g., OpenSSH, putty, SecureCRT) support these primitives.

## Enable Only Secure Cryptographic Primers on the IOS XE SSH Service

<ol>

<li>View the Cat9K SSH Status. </li>
Observe the large number of cryptographic primitives that are options for each algorithm.
<br>
<code>show ip ssh</code>
<br><br>
<img src="/images/01-01-show-ip-ssh-web.png" alt="SSH Server Configuration Status" width=600>
<br><br><br>


<li> View the SSH Hardening Playbook using cat. </li>
Note the following things in the Playbook
<ul>
<li>Call to the encrypted vault for authentication credentials</li>
<li>Usage of cisco.ios.ios_config: and lines:</li>
<li>IOS XE commands to force SSH to use strong primers</li> 
</ul>

<br>
<code>cat playbooks/01a-config-hard-ssh.yaml</code>
<br><br>
<img src="/images/01-02-cat-playbook-ssh-harden-web.png" alt="Playbook that Hardens IOS XE SSH Server" width=600>
<br><br><br>


<li>Now run the playbook.</li>
This playbook will ensure that each algorithm uses highly secure primitives.
You will be prompted for the vault password, the password is <b>abcd9876</b>.
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/01a-config-hard-ssh.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/01-03-playbook-output-web.png" alt="Playbook Ran Successfully" width=600>
<br><br><br>


<li>View the Cat9K SSH Status After Hardening. </li>
Note that the number of enabled cryptographic primitives for each algorithm has significantly decreased compared to the previous configuration. This change has been made on the Cat9K device to ensure that only the strong algorithms are enabled.
<br>
<code>show ip ssh </code>
<br><br>
<img src="/images/01-04-show-ip-ssh-web.png" alt="SSH Server Configuration Status" width=600>
<br><br><br>

## Enable Only Secure Ciphersuites on the IOS XE HTTPS Service

<li>View the Cat9K HTTPS Status. </li>
Notice that there are a large number of cipher suites enabled. Please note that the enabled cipher suites have of various categories: 'Recommended', 'Secure', and 'Weak'.
<br>
<code>sh ip http server status | sec secure</code>
<br><br>
<img src="/images/01-05-show-ip-https-web.png" alt="HTTPS Server Configuration Status" width=600>
<br><br><br>


<li>View the HTTPS Hardening Playbook using cat.  </li>
<br>
<code>cat playbooks/01b-config-hard-https.yaml</code>
<br><br>
<img src="/images/01-06-cat-playbook-https-harden-web.png" alt="Playbook that Hardens IOS XE HTTPS Server" width=600>
<br><br><br>


<li>Run the Harden HTTPs playbook.</li>
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/01b-config-hard-https.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/01-07-https-playbook-output-web.png" alt="Playbook Ran Successfully" width=600>
<br><br><br>


<li>View the Cat9K HTTPS Status After Hardening.</li>
Notice that the number of CipherSuites is much less than when we started. Now the ciphersuites we have enabled are 'Recommended' or 'Secure'.
<br>
<code>sh ip http server status | sec secure</code>
<br><br>
<img src="/images/01-08-show-ip-https-web.png" alt="Hardened HTTPS Server Configuration Status" width=600>
<br><br><br>



</ol>

[Click here to move on to the next section. Optimizing Local Authentication. ](/02-Local_Auth.md)
