# Cisco Live US 2023
# DEVWKS-2008 - Reducing the Attack Surface of IOS XE with Ansible

Thank you for spending your time with me for the next 45 minutes. I hope that at the end of 
this time you will be much more comfortable with hardening the IOS XE boxes that you manage. 

Please click the link below to find your Pod assignment and the network diagram. 

[Network Diagram & Pod Assignments](/labs-pods.md)

## [01. Harden the IOS XE Services](/01-Harden_Services.md)
SSH and HTTPS both use ciphers for encryption, some ciphers are more secure than others. By default IOS XE 
has ciphers enabled that favor compatibility over high security. In this exersize we will flip that switch
and 

## [02. Configure Common Criteria Policy & Local Users](/02-Local_Auth.md)
The local users on our IOS XE boxes need to comply with the same password policies that our 
typical Active Directory users comply with. Common Criteria allows us to enforce password 
policies on IOS XE. This will make InfoSec & auditors happy :) 

## [03. Enable Type 6 Passwords](/03-Type6_Passwords.md)
Type 5 & 7 passwords should not be used anywhere!  Type 6 passwords are AES-128 encrypted and are secure. 
In this exercise we will enable Type 6 passwords globally on the IOS XE box.

## [04. Configure MACsec on a VLAN Trunk Port](/04-MACsec_PSK.md)
MACsec is a layer 2 encryption protocol.  Catalyst 9000 switches have MACsec built in and are able to do 
line rate AES-128 (Cat9200), or AES-256 encryption on all ports at the same time. In this exercise we 
will enable MACsec on a switch to switch link. 

# FYI
  
## [Ansible Directory Structure](/Directory_Structure.md)