## Windows Server 2022 Hyper-V + Active Directory Lab

## Project Overview

This project demonstrates a fully functional enterprise-style virtualized infrastructure built using Windows Server 2022 running on a Dell PowerEdge R720 server with 
Hyper-V role enabled. The environment includes domain services, DNS, virtual machines, and client domain integration.

The lab simulates a real-world IT enterprise setup used for:

- Active Directory administration

- Domain controller configuration

- Hyper-V virtualization management

- Network and DNS services

- Client-server domain authentication


## Technologies Used

- Windows Server 2022

- Active Directory Domain Services (AD DS)

- DNS Server Role

- Hyper-V Virtualization

- Windows 11 Virtual Machine

- PowerShell Administration

- Virtual Networking (External Switch)

## Key Features Implemented

- Active Directory Domain Controller setup

- DNS integrated with AD

- Hyper-V virtualization environment

- External virtual switch networking

- Windows 11 VM deployment

- Domain join and authentication


- Network configuration with static IP


## Screenshots & Commands

![IPCONFIG](screenshots/hyper-v/NESTEDHOSTVM-ON-DC1.png)


## 1. Hyper-V Virtual Machines

Get-VM
![IPCONFIG](screenshots/hyper-v/VIRTUALISATION-CAPABILITY.png)

## 2. VM Processor Virtualization

Get-VMProcessor -VMName "NestedHostVM" | fl ExposeVirtualizationExtensions

![IPCONFIG](screenshots/hyper-v/VIRTUALISATION-CAPABILITY.png)



## 4. Active Directory Role

## Organizational Units (OUs)
- IT_DELL
- HR_DELL
- SALES_DELL

## Users Created
- ITDELLUSER1 → IT_DELL
- HRDELLUSER1 → HR_DELL
- SALESDELLUSER1 → SALES_DELL

---

##  Group Policy Configuration

##  IT Department (Full Access)
- Control Panel: Enabled
- Command Prompt: Enabled
- Full administrative-style access

![IPCONFIG](screenshots/active-directory/GROUP-POLICY-TESTED-ITDELLUSER1.png)

##  HR Department (Restricted Access)
- Control Panel: Disabled
- Command Prompt: Disabled
- Highly restricted system access for security compliance

![IPCONFIG](screenshots/active-directory/GROUP-POLICY-TESTED-HRDELLUSER1.png)

##  SALES Department (Standard Access)
- Control Panel: Disabled
- Command Prompt: Enabled
- Balanced user environment for business operations


![IPCONFIG](screenshots/active-directory/LOGGEDIN-AS-SALESDELLUSER1.png)

![IPCONFIG](screenshots/active-directory/GROUP-POLICY-TESTED-SALESDELLUSER1.png)




## 5. Domain Verification

Get-ADDomain

![IPCONFIG](screenshots/ip-config/IPCONFIG-HYPER-V-PC.png)

## 6. Virtual Switches

Get-VMSwitch

![IPCONFIG](screenshots/hyper-v/VM-SWITCH.png)

## 7. VM Network Adapter

Get-VMNetworkAdapter -VMName "NestedHostVM"

![IPCONFIG](screenshots/hyper-v/NETWORK-ADAPTER-BINDING.png)


## 9. Host System Info

Get-ComputerInfo | select WindowsProductName, WindowsVersion, CsName, CsDomain

![IPCONFIG](screenshots/dhcp/SCOPE_FOR_DHCP.png)

## 10. DNS Validation

nslookup ravikumar.local

![IPCONFIG](screenshots/dhcp/SCOPE_FOR_DHCP.png)

## 11. Group Policy Check

gpresult /r

![IPCONFIG](screenshots/dhcp/SCOPE_FOR_DHCP.png)

## 12. IP Configuration (Client)

ipconfig /all

![IPCONFIG](screenshots/ip-config/IPCONFIG-HYPER-V-PC.png)






## Skills Demonstrated

- Windows Server Administration

- Active Directory Management

- DNS Configuration

- Hyper-V Virtualization

- Virtual Machine Deployment

- Network Configuration (Static IP / External Switch)

- Domain Joining & Authentication

- System Monitoring & Troubleshooting

- PowerShell Automation

## Infrastructure Design

## Project Outcome

This lab demonstrates a complete enterprise-style IT infrastructure environment, simulating real-world scenarios used in corporate networks. It is suitable for showcasing 

skills for:

- IT Helpdesk Technician roles

- Junior System Administrator roles

- Desktop Support Engineer roles

- Infrastructure / Virtualization support roles

## Notes

- VM networking uses External Virtual Switch

- Domain: ravikumar.local

- Domain Controller: DC1

- Hyper-V enabled on physical server host

- Windows 11 VM is domain joined client

## Future Improvements

- Add multiple domain-joined clients

- Implement DHCP server role

- Configure Group Policy Objects (GPO) in depth


- Add file server role (SMB shares)


- Implement backup automation

- Create nested virtualization lab (Hyper-V inside VM)

## Author

Ravi Kumar

