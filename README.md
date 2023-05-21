**Project Name: Security Compliance Project (SecureOps-Ansible)**

This project aims to ensure security compliance for IIT Bombay Security by implementing various hardening activities on different servers and web applications.
**The project structure consists of four roles, each corresponding to a specific activity:**
Database_Server_Hardening
OS_Hardening
Web_Application_Hardening_Activities
Web_Server_Application_Hardening

**File Structure**
**Database_Server_Hardening/:** Contains the scripts and configurations related to hardening activities for the database server.
**OS_Hardening**/: Includes the necessary files for hardening the operating system of the servers.
**Web_Application_Hardening_Activities**/: Contains the scripts and configurations for hardening web applications.
**Web_Server_Application_Hardening**/: Includes the necessary files for hardening the web server.

**Usage**
To use this project, follow the steps below:

Ensure that Ansible and boto3  is installed on your system.
Clone this repository to your local machine.
Open the root directory of the project.
Run the following command in the terminal:
`ansible-playbook -i inventory playbook.yaml`
Sit back and relax while Ansible performs the necessary hardening activities.

**Project Overview**
This project focuses on ensuring security compliance by implementing a set of hardening activities for different server components. The activities performed include the following:

**Operating System (OS) Hardening Activities**
1. Updating the OS with the latest security patches.
2. Creating separate volumes for /var, /var/log, and /home.
3. Creating separate volumes for /tmp, /var/tmp, and /dev/shm with nodev, nosuid, and noexec options.
4. Disabling automounting for CD/DVDs and USB.
5. Setting a password for single-user mode.
6. Configuring stateful firewall rules.
7. Configuring SELinux.
8. Setting kernel tuning parameters.
9. Enabling and configuring Auditd and Syslogs.
10. Configuring OpenSSH securely.
11. Disabling unused services and network protocols.
12. Configuring Network Time Protocol (NTP).
13. Restricting crond access to authorized users.
14. Ensuring each user has a distinct user account.
15. Enforcing strong and periodic password changes.
16. Setting appropriate file permissions for users' dot files.
17. Using sudo access policy for admin-level tasks.
18. Removing world-writable files.
19. Removing unowned files and directories.
20. Setting sticky bit permission on world-writable directories.
21. Configuring Intrusion Prevention System (IPS) like Fail2Ban.
22. Configuring File System Integrity Checking like AIDE.

**Web Server Application Hardening Activities**
1. Updating the web server with the latest security patches.
2. Running the web server as a non-root user.
3. Disabling unnecessary modules on the web server.
4. Disabling web server directory listing.
5. Setting proper permissions for the Document Root directory.
6. Disabling HTTP Trace method.
7. Disabling HTTP Proxy Server.
8. Avoiding software/OS version advertisement by the web server.
9. Installing and enabling mod_security.
10. Removing default web server content.
11. Configuring web server syslog facility.
12. Configuring SSL/TLS securely.

**Database Server Hardening Activities**
1. The Database Server Hardening activities focus on securing the database server by implementing various measures. These activities include:
2. Update Database Server: Ensure the database server is updated with the latest security patches.
3. Disable Unnecessary Modules: Disable or remove unnecessary modules from the database server.
4. Dedicated User Account: Run the database server daemon with a dedicated least privileged account.
5. Safe Mode: Ensure the database server daemon is not started with safe mode.
6. Remove Default Databases and Users: Remove default databases and users from the database server.
7. No Wildcard Hostnames: Ensure no users have wildcard hostnames in the database server.
8. Disable Command History: Disable command history in the database server.

**Web Application Hardening Activities**
1. The Web Application Hardening activities aim to enhance the security of web applications. The following measures are implemented:
3. Update Applications: Update applications and their 3rd party plugins, codes, etc., with the latest security patches.
4. Input Parameter Validation: Implement proper validation on all input parameters in both client and server sides.
5. HTTP Security Headers: Implement proper HTTP Security Headers in the application.
6. Error Handling: Implement proper error-handling mechanisms in the application.
7. Secure Password Storage: Avoid storing plain passwords in config files, source code, or databases.
8. Disable Directory Traversal: Disable directory traversal in the application.
9. Encrypted Communication: Ensure all communications are done through an encrypted channel when integrating with 3rd party applications or using APIs for external communication.
10. Secure Login Functionality: Implement secure login functionality, including CAPTCHA, proper session timeouts, restricted access to admin URLs, and storing hashed passwords in the database.
11. Disable Application Version Information: Disable or remove application version information files.
12. Proper Permission Settings: Set proper permissions on application directories and files.
13. No Public File Upload: Avoid file upload in public modules of the application.
14. Disable Non-Required Methods: Disable non-required methods like TRACE, PUT, DELETE in the application or web server.
15. Disable Directory Listing: Disable directory listing in the application.
16. Minimum Access Restriction: Restrict each application to minimum access, allowing access only from the required networks.
17. Non-Root User: Ensure the application process runs as a non-root user.
18. CAPTCHA on Entry-Forms: Implement CAPTCHA on all entry-forms in public pages.
19. Secure Email Addresses: Replace email addresses with images and replace "@" with "[at]" and "." with "[dot]".

*P.S: OS_Hardning is for ubuntu and debian.
Web_Server_Hardning is for nginx*
