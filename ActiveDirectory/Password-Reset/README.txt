LAB: Password Reset & Account Unlock (Active Directory)

AUTHOR: Mark Gutierrez

---

OVERVIEW:

This lab demonstrates how to handle a common IT support scenario involving a locked-out user account. The objective was to simulate failed login attempts, trigger an account lockout, and perform administrative recovery by unlocking the account and resetting the password in Active Directory.

---

OBJECTIVES:

* Simulate user account lockout due to failed login attempts
* Identify lockout status in Active Directory
* Reset user password
* Unlock user account
* Verify successful login on client machine
* Analyze security events in Event Viewer

---

ENVIRONMENT:

* Windows Server 2022 (Domain Controller)
* Windows 10 (Client Machine - CLIENT02)
* Domain: corp.local
* Tools Used:

  * Active Directory Users and Computers (ADUC)
  * Group Policy Management (GPMC)
  * Event Viewer
  * Command Prompt (whoami, gpresult)

---

STEPS PERFORMED:

1. Account Lockout Simulation

   * Attempted multiple failed logins on CLIENT02
   * Triggered account lockout based on domain policy

2. Lockout Verification

   * Accessed Active Directory Users and Computers
   * Navigated to HR Organizational Unit (OU)
   * Verified account lockout status under user properties

3. Password Reset & Account Unlock

   * Reset user password via ADUC
   * Enabled "User must change password at next logon"
   * Unlocked the user account

4. Client Login Verification

   * Logged into CLIENT02 using updated credentials
   * Successfully authenticated into the domain
   * Verified user identity using:

     * Command: whoami

5. Event Log Analysis

   * Opened Event Viewer on Domain Controller
   * Navigated to:
     Windows Logs → Security
   * Identified:

     * Event ID 4740 (Account Locked Out)
   * (Optional) Verified failed login attempts on client (Event ID 4625)

---

RESULTS:

* Successfully simulated and resolved a user account lockout
* Restored user access through password reset and account unlock
* Verified authentication from client machine
* Confirmed security events in Event Viewer

---

KEY CONCEPTS:

* Active Directory User Management
* Account Lockout Policies
* Password Reset Procedures
* Authentication & Security Logging
* Event Viewer Analysis
* Client-Server Interaction in Domain Environments

---

LESSONS LEARNED:

* Account lockout events are logged on the Domain Controller (Event ID 4740)
* Failed login attempts (Event ID 4625) may appear on the client machine
* Proper group membership and GPO settings affect login behavior
* Verifying actions across both server and client is critical in troubleshooting

---

SCREENSHOTS INCLUDED:

* AD_Account_Locked.png
* Password_Reset_and_Account_Unlock.png
* Password_Reset_Prompt_Successful.png
* Whoami_Verification.png

---
