# Configure a Common Criteria Policy and Local Users 

Your Active Directory enforces password compliance. Your IOS XE box can too!

IOS XE supports Common Criteria Policies and they allow Network Engineers to configure options such as minimum and maximum password lengths, max number of times a character can be consecutively repeated and force use of upper, lower, numberic and special characters. 
<br><br>
In this task we will view and run a playbook that will create a Common Criteria Policy and a local user with a password that is compliant. 

## Create a Common Criteria Policy Based on Business Requirements

<ol>

<li>View the Playbook that will Create the Common Criteria Policy</li>
<br>
<code>cat playbooks/02a-add-common-criteria-policy.yaml</code>
<br><br>
<img src="/images/02-01-cat-common-criteria-playbook-web.png" alt="" width=600>
<br><br><br>

<li>Run the Playbook that will Create the Common Criteria Policy </li>
<br>
<code>ansible-playbook -i inventories/devnet-switches.yaml playbooks/02a-add-common-criteria-policy.yaml --ask-vault-pass</code>
<br><br>
<img src="/images/02-02-playbook-output-common-criteria-web.png" alt="" width=600>
<br><br><br>

<li>View the Common Criterial Policy on the Switch </li>
<br>
<code>show runn | sec aaa common-criteria</code>
<br><br>
<img src="/images/02-03-show-run-common-criteria-web.png" alt="" width=600>
<br><br><br>

## Create a Local User, with Priv 15, whose password complies with Common Criteria 

<li>View the Playbook that will Create the IOS XE Local User </li>
<br>
<code>cat playbooks/config-common-criteria-users.yaml</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>


<li>Run the Playbook that will Create the IOS XE Local User </li>
<br>
<code>ansibile-playbook -i inventories/devnet-switches.yaml playbooks/config-common-criteria-users.yaml --ask-vault-pass</code>
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
<code>cat playbooks/config-login-block.yaml</code>
<br><br>
<img src="/images/" alt="" width=600>
<br><br><br>

<li>Run the Playbook that will Configure Login Block </li>
<br>
<code>ansibile-playbook -i inventories/devnet-switches.yaml playbooks/config-login-block.yaml --ask-vault-pass</code>
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

[Click here to move on to the next section. Configuring Switchport Trunk with MACsec. ](/05-MACsec_PSK.md)
