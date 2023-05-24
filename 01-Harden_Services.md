# Harden IOS XE SSH & HTTPS Services

Now it's time to run some Ansible Playbooks and Reduce the Attack Surface of the IOS XE box! <br>

The SSH server on IOS XE supports several cryptographic primers that are enabled for compatibility reasons. Some of these are less secure than others. In this task we will run a playbook that will modify the SSH server to only use highly secure cryptographic primers. Modern versions of the popular SSH clients (eg. OpenSSH, putty, SecureCRT) supported these primers.

## Enable Only Secure Cryptographic Primers on the IOS XE SSH Service

<ol>

<li>View the Cat9K SSH Status. </li>
Observe the large number of primers that are options for each algorithm.
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
<code>cat playbooks/01-config-hard-ssh.yaml</code>
<br><br>
<img src="/images/01-02-cat-playbook-ssh-harden-web.png" alt="" width=600>
<br><br><br>


<li>Now run the playbook.</li>
This playbook will assure that each of the algorithms are using highly secure primers.
You will be prompted for the vault password, recall we set that before, the password is <b>abcd9876</b>.
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/01-config-hard-ssh.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/01-03-playbook-output-web.png" alt="Playbook Ran Successfully" width=600>
<br><br><br>


<li>View the Cat9K SSH Status After Hardening. </li>
Notice that the number of cryptographic primers that are enabled for each algorithm are much less than before. We have assured that only the stong algorithms are enabled. 
<br>
<code>show ip ssh </code>
<br><br>
<img src="/images/01-04-show-ip-ssh-web.png" alt="SSH Server Configuration Status" width=600>
<br><br><br>

## Enable Only Secure Ciphersuites on the IOS XE HTTPS Service

<li>View the Cat9K HTTPS Status. </li>
<br>
<code>show ip http server status</code>
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

[Click here to move on to the next section. Optimizing Local Authentication. ](/04-Local_Auth.md)
