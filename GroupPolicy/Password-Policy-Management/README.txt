LAB: Password Policy Management via Group Policy (Active Directory)

AUTHOR: Mark Gutierrez

---

OVERVIEW:

This lab demonstrates how to configure and enforce password policies in an Active Directory environment using Group Policy. The objective was to define security requirements such as password complexity, minimum length, and account lockout thresholds to enhance system security.

---

OBJECTIVES:

* Configure password policy settings using Group Policy
* Enforce password complexity requirements
* Set minimum password length and expiration policies
* Configure account lockout threshold and duration
* Apply and verify Group Policy settings on client machines
* Validate policy enforcement through user login behavior

---

ENVIRONMENT:

* Windows Server 2022 (Domain Controller)
* Windows 10 (Client Machine - CLIENT02)
* Domain: corp.local
* Tools Used:

  * Group Policy Management (GPMC)
  * Active Directory Users and Computers (ADUC)
  * Command Prompt (gpupdate, gpresult)
  * Local Security Policy (for comparison)

---

STEPS PERFORMED:

1. Group Policy Configuration

   * Opened Group Policy Management Console (GPMC)
   * Edited Default Domain Policy (or created a custom GPO)
   * Navigated to:
     Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies

2. Password Policy Setup

   * Enabled password complexity requirements
   * Set minimum password length
   * Configured maximum password age
   * Defined password history requirements

3. Account Lockout Policy Configuration

   * Set account lockout threshold (number of failed attempts)
   * Configured lockout duration and reset time

4. Policy Application

   * Linked GPO to domain or appropriate Organizational Unit (OU)
   * Forced policy update using:

     * Command: gpupdate /force

5. Policy Verification

   * Logged into CLIENT02 and tested password requirements
   * Attempted weak passwords to confirm enforcement
   * Verified applied policies using:

     * Command: gpresult /r

---

RESULTS:

* Successfully configured and applied password policies using Group Policy
* Enforced password complexity and security requirements
* Verified policy application on client machine
* Confirmed account lockout behavior based on defined thresholds

---

KEY CONCEPTS:

* Group Policy Management
* Password Policy Enforcement
* Account Lockout Configuration
* Domain-Level Security Policies
* Policy Application & Verification
* Active Directory Security Best Practices

---

LESSONS LEARNED:

* Password policies are typically enforced at the domain level via Default Domain Policy
* Group Policy changes require gpupdate or system restart to apply immediately
* gpresult is essential for verifying applied policies
* Proper configuration of lockout settings is critical to balance security and usability

---

SCREENSHOTS INCLUDED:

* GPO_Password_Policy_Settings.png
* Account_Lockout_Policy.png
* GPUpdate_Force.png
* GPResult_Verification.png

---
