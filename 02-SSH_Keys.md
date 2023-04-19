# Working with SSH Keys

When connecting to an SSH Server the first time the client typically doesnt have the servers public key. In Ansible this results in an error, but one that we can easily and securely solve. Let's dig in.  This client needs to have a stored copy of the servers key in order to authenticate the server and prevent a meddler-in-the-middle attack. 

<ol>

<br>
<li>Let's take a look at the error that Ansible throws when the key isn't stored.</li>
<br>
<img src="/images/02-01-ssh-key-error-web.png" alt="SSH Key Unknown Error" width=600>
<br><br><br>

<li>Each time you connecto to a new SSH server the servers public key is stored in the known_hosts file. Use the cat command to view the keys that are in the known_hosts file.</li>
<br>
<code>cat ~/.ssh/known_hosts</code>
<br><br>
<img src="/images/02-02-cat-ssh-known-hosts-web.png" alt="Contents of SSH Known Hosts File" width=600>
<br><br><br>

<li> </li>

<img src="/images/" alt="" width=600>
<img src="/images/" alt="" width=600>
<img src="/images/" alt="" width=600>


</ol>
