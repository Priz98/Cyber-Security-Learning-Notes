# A02 - Security Misconfigurations

## What is a Security Misconfiguration?

Security Misconfiguration occurs when a system, application, cloud service is not securely
configured at any stage of its lifecycle, resulting in potential security vulnerabilities.

## A Security Misconfiguration can be caused if : 

1. Lack of proper Security Hardening.
2. Improperly assigned permission.
3. Using default accounts and passwords.
4. Overcomplicating application structure, leaving open port.
5. Using legacy applications.
6. Once upgraded not setting up corresponding security configurations.
7. Lack of Security header from Servers.
8. Unsecure methods for production like libs and such.
9. Overly Informative Error Handling to end user.

## Ways to prevent Security Misconfigurations.

1. Reduce the attack surface itself.
2. Different environments should be configured identically to avoid any unexpected behaviour.
3. Repeatable hardening process can be automated to keep it more cosistent.
4. A task to check all the updated application's security configuration, Also to check any changes cloud services or permissions.
5. Proactively add a central configuration to intercept excessive error messages as a backup and also to log them.
6. Use Short lived credentials or token, Use Role based access controls, instead of static embeded keys.

## Attack Scernario

Directory listing is not disabled on the server. An attacker discovers they can simply list directories. The attacker finds and downloads the compiled Java classes, which they decompile and reverse engineer to view the code. The attacker then finds a severe access control flaw in the application.

## My Understanding

The attacker is not specifically looking for source code. They are trying to collect any information that helps them understand the application better.

In this case, directory listing allowed the attacker to see files that should not have been publicly visible. The attacker downloaded the compiled Java files and decompiled them to learn how the application works internally.

Even though the files were not source code, they still contained useful information. By studying the application's logic, the attacker was able to identify an access control weakness and use that knowledge to further attack the application.

The main lesson is that attackers do not stop just because they don't immediately find something valuable. They often collect every piece of information they can and combine it to discover vulnerabilities.



