# Configure a Common Criteria Policy and Local Users 

Your Active Directory enforces password compliance. Your IOS XE box can too!<br>
IOS XE supports Common Criteria Policies and they allow Network Engineers to configure options such as minimum and maximum password lengths, max number of times a character can be consecutively repeated and force use of upper, lower, numberic and special characters. 
<br><br>
In this task we will view and run a playbook that will create a Common Criteria Policy and a local user with a password that is compliant. 

<ol>

<li>View the Playbook that will Create the Common Criteria Policy</li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>Run the Playbook that will Create the Common Criteria Policy </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>View the Common Criterial Policy on the Switch </li>
<br>
<code>show runn | sec aaa common-criteria</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>View the Playbook that will Create the IOS XE Local User </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>Run the Playbook that will Create the IOS XE Local User </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>View the Local User </li>
Notice how some of the users do not have the Common Criteria applied and that the one we just created does have it applied. 
<br>
<code>show runn | inc username</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>View the Playbook that will Configure Login Block  </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>Run the Playbook that will Configure Login Block </li>
<br>
<code></code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>View the Login Block Configuration  </li>
<br>
<code>show runn | INSERT PROPER COMMANDS HERE</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>






</ol>
