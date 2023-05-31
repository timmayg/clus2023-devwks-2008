# Cisco Live US 2023
# DEVWKS-2008 - Reducing the Attack Surface of IOS XE with Ansible

Thank you for spending the next 45 minutes with me. Once we are complete, 
you will be much more comfortable Reducing the Attack Surface on the IOS XE 
boxes you manage.

Please click the link below to find your Pod assignment and the network diagram. 

[Network Diagram & Pod Assignments](/labs-pods.md)


## [01. Harden the IOS XE Services](/01-Harden_Services.md)
SSH and HTTPS both use ciphers for encryption; some ciphers are more secure than others. By default, IOS XE  has ciphers enabled that favor compatibility over high security. In this exercise, we will flip that switch and ensure that only the strongest ciphers are allowed. I've tested this, and all modern clients will work just fine. 


## [02. Configure Common Criteria Policy & Local Users](/02-Local_Auth.md)
The local users on our IOS XE boxes must comply with the same password policies our typical Active Directory users comply with. Common Criteria allows us to enforce password policies on IOS XE. Displaying this compliance on our IOS XE boxes will make InfoSec & auditors happy. :)


## [03. Enable Type 6 Passwords](/03-Type6_Passwords.md)
We must stop using Type 5 hashing & Type 7 obfuscation. Type 6 passwords are AES-128 encrypted and secure. This exercise will enable Type 6 passwords globally on the IOS XE box. 


## [04. Configure MACsec on a VLAN Trunk Port](/04-MACsec_PSK.md)
MACsec is a Layer 2 encryption protocol. Catalyst 9000 switches have MACsec built in and can do line rate AES-128 or AES-256 encryption on all ports; this can equal terabits of encryption on a single Cat 9000. In this exercise, we will enable MACsec on a switch-to-switch link. 

# FYI
  
## [Ansible Directory Structure](/Directory_Structure.md)