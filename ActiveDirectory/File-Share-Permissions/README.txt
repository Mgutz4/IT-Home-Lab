LAB NAME: Group Policy & File Share Lab

OVERVIEW:
This lab demonstrates the use of Group Policy Objects (GPOs) to automate drive mapping and manage user access to shared resources.

OBJECTIVE:
- Create and link GPO
- Configure mapped network drive
- Apply policy to HR users
- Troubleshoot access issues

ENVIRONMENT:
- Domain: corp.local
- Server: Windows Server 2022
- Client: Windows 10 (CLIENT02)

CONFIGURATION:
- Created shared folder: C:\HR_Share
- Configured permissions:
  - HR group → Full Control
- Created GPO: HR Drive Mapping
- Mapped drive:
  - H: → \\SERVER01\HR_Share
- Linked GPO to HR OU

TESTING:
- Ran gpupdate /force
- Verified drive mapping on CLIENT02
- Tested file creation and modification

TROUBLESHOOTING:
- Diagnosed "Access Denied" error
- Verified group membership (whoami /groups)
- Corrected NTFS and share permissions
- Refreshed user session

RESULT:
- Drive successfully mapped
- HR users can access and modify files

SKILLS DEMONSTRATED:
- Group Policy Management
- NTFS vs Share permissions
- Active Directory groups
- Troubleshooting access issues