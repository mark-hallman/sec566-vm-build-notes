# SEC566 Windows 11 VM Requirements

This issue captures the requirements for the J01 build of the SEC566 Windows Auditor VM.  It will be updated from time to time.  This information is also be posted on Jira.  

## General Info
Windows 11 Enterprise - fully patched, activated with SANS License Key
SIS Turn-in Date: 

## Account / User Information
- [x] User = Auditor
- [x] Pass = Sec566!! 
- [x] Computername = Windows Auditor
- [x] Blue Desktop color, possible graphics to follow

## Applications to Install
- [x] WireShark
- [x] OpenVPN
- [x] nmap
- [x] ngrep
- [x] Windows Terminal
- [x] git
- [x] VS Code
- [x] Search Everything
- [x] Firefox

## Win11 Configuration
- [ ] No WSL - What about the EWB?  Could use pure PowerShell like we did in 670
- [ ] Enable RDP in/out
- [ ] Disable Windows Defender
- [ ] Disable Windows Update
- [x] Desktop shortcuts and items pinned to the task bar.
  - [x] RDP
  - [x] Wireshark
  - [x] Edge
  - [x] Firefox
  - [x] nmap
  - [x] Everything
  - [x] VS Code


## 2024-06-26 10:25:44 - Additional Requirements

- [x] Add to C:\Tools\ 
  - [x] Nipper
  - [x] Parse-nmap
- [x] Install CSAT from CIS
  - [x] Install prereq  Neo4j
  - [x] Add the license file
  - [ ] Add the self-signed cert to trusted certs
  - [ ] Add the CSAT icon to the task bar
- [ ] Add the OpenVPN icon to the task bar
- [ ] Turn on RDP
- [x] Change the Windows password to "Sec566!!"
- [x] These should be on the task bar
  - [x] Firefox
  - [x] Edge
  - [x] Terminal
  - [x] VS Code
  - [x] Everything
  - [x] Code
  - [x] Wireshark
  - [x] nmap GUI
  - [x] RDP
  - [x] OpenVPN
- [x] Firefox and Edge should have bookmarks:
  - [x]  EWB
  - [x]  CSAT


CSAT needs to be installed and the license file is here for the install. The install notes are linked in the user guide. Passwords should be the same password as the VM (and can we change the VM password to 'Sec566!!' without the quotes. That will match the Cloud creds. Thanks.

CSAT will open a web port for localhost... Also it installs a certificate. Will you please add the cert to trusted certs so we do not get an error message when connecting. LAB 1.1 is the lab that uses the tool if you want to test it.

trust it the self signed cert for CSAT


- [x] All passwords "Sec566!!"


