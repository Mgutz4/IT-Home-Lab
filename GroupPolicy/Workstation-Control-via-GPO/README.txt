Lab Title: Workstation Access Control via Group Policy

Objective:
Configure a Group Policy Object (GPO) to restrict workstation logon access to only authorized HR users.

Environment:
- Windows Server 2022 (Domain Controller)
- Windows 10 Client (CLIENT02)
- Domain: corp.local

Steps Performed:
1. Created HR security group and added users (Maria Lopez, Jacob Wright)
2. Created Workstations OU and moved CLIENT02 into it
3. Created GPO: "Restrict Logon to HR Users"
4. Configured:
   Computer Configuration → Policies → Windows Settings → Security Settings → Local Policies → User Rights Assignment
   - Allow log on locally → HR group + Administrators
5. Linked GPO to Workstations OU
6. Forced Group Policy update (gpupdate /force) and rebooted client
7. Tested logon behavior:
   - Non-HR users denied access
   - HR users successfully logged in

Troubleshooting:
- Identified GPO not applying due to OU scope
- Resolved by moving CLIENT02 into correct OU
- Verified policy application using gpresult /r

Result:
Successfully enforced department-based access control using Group Policy.

Skills Demonstrated:
- Active Directory (Users, Groups, OUs)
- Group Policy Management
- Security Filtering & User Rights Assignment
- Troubleshooting GPO application
- Windows Client Administration