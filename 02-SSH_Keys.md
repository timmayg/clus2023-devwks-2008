# Working with SSH Keys

When connecting to an SSH Server the first time the client typically doesnt have the servers public key. In Ansible this results in an error, but one that we can easily and securely solve. Let's dig in.  This client needs to have a stored copy of the servers key in order to authenticate the server and prevent a meddler-in-the-middle attack. 

<ol>

<br>
<li>Let's take a look at the error that Ansible throws when the key isn't stored.</li>
The error Ansible throws at us is very clear in the issue, "The authenticity of the host cannot be established due to the host being unknown." 
<br>
<img src="/images/02-01-ssh-key-error-web.png" alt="SSH Key Unknown Error" width=600>
<br><br><br>

<li>Each time you connecto to a new SSH server the servers public key is stored in the known_hosts file. Use the cat command to view the keys that are in the known_hosts file.</li>
<br>
<code>cat ~/.ssh/known_hosts</code>
<br><br>
<img src="/images/02-02-cat-ssh-known-hosts-web.png" alt="Contents of SSH Known Hosts File" width=600>
<br><br><br>

<li>Add tcp/22 SSH Public Key to the Known Hosts File for Cat9300-1</li>
THe output of this command shows us that we are using SSH version 2 and that the 'server' is running Cisco software. 
<br>
<code>ssh-keyscan -p 22 10.1.1.5 >> ~/.ssh/known_hosts </code>
<br><br>
<img src="/images/02-03-ssh-keyscan-web.png" alt="" width=600>
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
