LAB NAME: RDP & DNS Troubleshooting Lab

OVERVIEW:
This lab demonstrates troubleshooting Remote Desktop (RDP) connectivity issues caused by DNS misconfiguration in a Windows client environment.

OBJECTIVE:

* Identify DNS misconfiguration
* Troubleshoot lack of internet connectivity
* Test network communication using ping
* Fix DNS issues
* Enable and test Remote Desktop (RDP)
* Resolve authentication and NLA-related errors

ENVIRONMENT:

* Domain: corp.local
* Client: Windows 10 / Windows 11
* Machine Name: CLIENT02
* Tools: Command Prompt, IPv4 Settings, Remote Desktop

CONFIGURATION:

* Initial DNS set incorrectly to 192.168.56.10
* Correct DNS set to 192.168.50.10
* Remote Desktop enabled on target machine

TESTING:

* Verified connectivity using:

  * ping
* Flushed DNS using:

  * ipconfig /flushdns
  * ipconfig /registerdns
* Attempted Remote Desktop connection
* Observed RDP connection errors and NLA issue
* Retested after correcting DNS configuration

RESULT:

* Internet connectivity restored
* DNS resolving correctly
* Remote Desktop connection successful
* System accessible remotely

SKILLS DEMONSTRATED:

* DNS troubleshooting
* Remote Desktop (RDP)
* Network troubleshooting
* Windows client configuration
* Command-line tools (ipconfig, ping)

