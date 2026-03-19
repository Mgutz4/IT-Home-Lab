LAB NAME: Active Directory & DNS Resolution Lab

OVERVIEW:
This lab demonstrates the deployment of Active Directory Domain Services (AD DS) and DNS configuration in a Windows Server environment.

OBJECTIVE:
- Install and configure AD DS
- Promote server to Domain Controller
- Configure DNS for domain resolution
- Verify client-to-server communication

ENVIRONMENT:
- Domain: corp.local
- Server: Windows Server 2022 (Domain Controller)
- Client: Windows 10

CONFIGURATION:
- Installed AD DS role
- Promoted server to Domain Controller
- Configured DNS zone (corp.local)
- Set client DNS to Domain Controller IP

TESTING:
- Verified DNS using:
  - ping
  - nslookup
- Successfully joined client to domain
- Confirmed domain authentication

RESULT:
- Domain successfully deployed
- DNS resolving correctly
- Client communicating with Domain Controller

SKILLS DEMONSTRATED:
- Active Directory (AD DS)
- DNS configuration
- Domain join process
- Network troubleshooting