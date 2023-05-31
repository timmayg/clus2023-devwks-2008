## Labs & Pods

The lab network we will be working with looks like the diagram below. 
<img src="/images/network-diagram.png" alt="DEVWKS-2008 Network Diagram" width=600>

Please use this table to determine what Pod you have been assigned. 

## 01. Find your Workstation and then find your Pod FQDN in the table below. 

NOTE: Please do NOT use Pod 12 !!! 
Things will break, lab will fail!  
You've been warned! 

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



## 02. Please open 3 SSH Windows to your Pod. 

<img src="/images/10-01-lab-workstation-web.png" alt="Fresh Lab Workstation" width=600>

Run this 3 times, ADJUST for your Pod ## !

<code> ssh -p 3389 -l ciscolive podXX-xelab.cisco.com </code>

The first SSH session will be used for managing Ansible and the files. 

The second SSH session will be a jump box for you to get to the first Cat9300 switch. 

<code> ssh 10.1.1.5 </code>

The third SSH session will be a jump box for you to get to the second Cat9300 switch.

<code> ssh 10.1.1.55 </code>

SSH Username & Password for the Ubuntu & the Cat9300 switches are all the same.

### User: ciscolive

### Password: ciscolive123

I arrange my SSH sessions like this for best viewing.   Adjust them for your own preferences. 

<img src="/images/10-02-lab-workstation-ssh-web.png" alt="3 SSH Sessiosn on Lab Workstation" width=600>


## 03. Return back to the main page and then move on to step 1. 

[Main Page](/README.md)




