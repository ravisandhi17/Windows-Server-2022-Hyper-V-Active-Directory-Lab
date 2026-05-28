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

## 1. Hyper-V Virtual Machines

Get-VM

## 2. VM Processor Virtualization

Get-VMProcessor -VMName "NestedHostVM" | fl ExposeVirtualizationExtensions

## 3. Network Configuration

Get-NetIPConfiguration

## 4. Active Directory Role


Get-WindowsFeature AD-Domain-Services

## 5. Domain Verification

Get-ADDomain

## 6. Virtual Switches

Get-VMSwitch

## 7. VM Network Adapter

Get-VMNetworkAdapter -VMName "NestedHostVM"

## 8. VM Performance

Get-VM | Select Name, State, CPUUsage, MemoryAssigned, Uptime

## 9. Host System Info

Get-ComputerInfo | select WindowsProductName, WindowsVersion, CsName, CsDomain

## 10. DNS Validation

nslookup ravikumar.local

## 11. Group Policy Check

gpresult /r

## 12. IP Configuration (Client)

ipconfig /all

## 13. AD Domain Join (Client)

systeminfo | findstr /B /C:"Domain"

## 14. Authentication Check

whoami

## 15. System Event Logs

Get-WinEvent -LogName System -MaxEvents 20

## 16. Installed Roles

Get-WindowsFeature | Where Installed

## 17. Windows Updates

Get-HotFix

## 18. VM Checkpoints

Get-VMSnapshot -VMName "NestedHostVM"

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

