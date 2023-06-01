## Labs & Pods

The lab network we will be working with looks like the diagram below. 
<img src="/images/network-diagram.png" alt="DEVWKS-2008 Network Diagram" width=600>



<ol>

<li> Use this table to determine what Pod you have been assigned. </li>

NOTE: Please do NOT use Pod 12 !!! Things will break, lab will fail! You've been warned! 

| Workstation #  | Pod FQDN  |
| -------------- | ----------- |
| Workstation #1  | pod01-xelab.cisco.com   |
| Workstation #2  | pod02-xelab.cisco.com   |
| Workstation #3  | pod03-xelab.cisco.com   |
| Workstation #4  | pod04-xelab.cisco.com   |
| Workstation #5  | pod05-xelab.cisco.com   |
| Workstation #6  | pod06-xelab.cisco.com   |
| Workstation #7  | pod07-xelab.cisco.com   |
| Workstation #8  | pod08-xelab.cisco.com   |
| Workstation #9  | pod09-xelab.cisco.com   |
| Workstation #10  | pod10-xelab.cisco.com   |
| Workstation #11  | pod11-xelab.cisco.com   |
| Workstation #12  | pod13-xelab.cisco.com   |


<li>Open 3 SSH Windows to your Pod.  </li>

<img src="/images/10-01-lab-workstation-web.png" alt="Fresh Lab Workstation" width=600>

Run this 3 times, ADJUST for your Pod ## !

<code> ssh -p 3389 -l ciscolive podXX-xelab.cisco.com </code>

SSH Username & Password for the Ubuntu & the Cat9300 switches are all the same.
### User: ciscolive
### Password: ciscolive123

<li> The first SSH session will be used for managing Ansible and the files. </li>
We will need to change directories to the CLUS folder for this lab. 
<code> cd /clus2023-devwks-2008 </code>

<li> The second SSH session will be a jump box for you to get to the first Cat9300 switch. </li>

<code> ssh 10.1.1.5 </code>

<li> The third SSH session will be a jump box for you to get to the second Cat9300 switch.</li>

<code> ssh 10.1.1.55 </code>



I arrange my SSH sessions like this for best viewing.   Adjust them for your own preferences. 

<img src="/images/10-02-lab-workstation-ssh-web.png" alt="3 SSH Sessiosn on Lab Workstation" width=600>


</ol>


[Click here to move on to the next section. Harden Services](/01-Harden_Services.md)




