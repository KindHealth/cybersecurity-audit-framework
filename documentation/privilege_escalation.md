**Summary**

This is a simple markdown info on how to perform privilege escalation on the Windows and Linux operating systems. This markdown will cover the tools and vectors used in the this stage.

**Privilege Escalation Steps**

This stage revolves around getting code execution at a level higher than the current user. The goal being the highest level (SYSTEM/ROOT) possible on the system.
![Privilege Escalation](../resources/privilege_escalation.svg)

You can also download this map from the resources directory [here](../resources/privilege_escalation.svg).

Following sections will contain a breakdown of each node in the map. These sections will link programs/software/guides that help with this stage.

**Windows**
1. **Missing or outdated systems**
	* Most exploits can be defeated by staying at the most recent patch level
	* https://github.com/GDSSecurity/Windows-Exploit-Suggester
2. **Service Configuration**
	* If able to configure a service, the user can choose a new binary to run in its place
	* The new binary will run in the context of the service (SYSTEM)
	* https://docs.microsoft.com/en-us/sysinternals/downloads/accesschk
3. **GPO Preference File**
	* Auto generated file containing credentials used to apply GPP
	* https://adsecurity.org/?p=2288
4. **Weak credentials**
	* Vulnerable to password spray attacks
	* https://github.com/dafthack/DomainPasswordSpray
5. **DLL Hijacking**
	* http://www.greyhathacker.net/?p=738
	* https://www.fireeye.com/content/dam/fireeye-www/global/en/current-threats/pdfs/rpt-dll-sideloading.pdf
6. **Scheduled Tasks**
	* If a task uses a file that is writable by the attacker, the resource can be modified to gain code execution at the privilege of the task creator

**Linux**
1. **SUID Misconfiguration**
	* Intended to allow normal users to execute certain programs with elevated privileges
	* https://pentestlab.blog/2017/09/25/suid-executables/
2. **Kernel Exploit**
	* Many Linux systems run with outdated kernel versions
	* https://github.com/mzet-/linux-exploit-suggester
3. **Cron**
	* If a task uses a file that is writable by the attacker, the resource can be modified to gain code execution at the privilege of the task creator
4. **Restricted Shell Escape**
	* Restricted shells are common for systems with many low privilege users
	* https://pen-testing.sans.org/blog/2012/06/06/escaping-restricted-linux-shells
5. **Services running as root**
	* If an exploit exists for software running on the system, code execution can be achieved at the access level of the program
	* Outdated internal services are often overlooked in longstanding production environments
6. **Sudo rights/users**
	* Sudo rights can be given to normal users for specific commands, which can introduce unpredicted vulnerabilities
	* Users with Sudo rights and weak credentials can be  an easy target
