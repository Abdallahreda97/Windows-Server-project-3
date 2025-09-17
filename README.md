# Windows-Server-project-3
Overview

This project demonstrates the implementation of an Active Directory Domain Services (AD DS) environment with organizational units, group policies, DHCP, DNS load balancing, and user access configurations.
The lab simulates a corporate environment with three departments: HR, Sales, and IT.
Steps Implemented


1. Domain Setup

Created a new domain environment:

Domain Name: rev.local

Domain Controller (DC) Computer Name: PDC

IP Address: 192.168.1.2


2. Organizational Units & Users

Created separate OUs for each department:

HR, Sales, IT

Added multiple users under each OU.

Created security groups for each department and added respective users to their groups.


3. Client Machine Join

Joined a Windows 10 machine to the domain:

Computer Name: HRPC01


4. Group Memberships & Permissions

Added the IT-Group as a Local Administrator on client machines.

Applied restrictions using Group Policy:

Removed Properties from This PC context menu.

Disabled Command Prompt and Control Panel for HR and Sales.

Disabled External Storage access for HR, but excluded IT-Group.


5. Password & Account Policies

Configured domain password policy:

Change every 60 days

Minimum 6 characters, must be complex

Remember last 3 passwords

Configured Account Lockout policy:

Lock account for 30 minutes after 5 failed login attempts


6. HR Shortcut

Created an HR portal shortcut (http://hrapp.rev.local) on the desktop of all HR users.


7. DHCP Configuration

Configured DHCP with scope:

Range: 192.168.1.40 – 192.168.1.230 (/24)

Excluded: 192.168.1.80 – 192.168.1.85

Reserved IP for client machine:

192.168.1.200


8. DNS Load Balancing

Configured DNS round-robin load balancing for:

www.rev.local

IP Addresses: 192.168.1.8 and 192.168.1.9


9. File Sharing

Created a Mapped Drive for all users named Public.

Applied permissions:

Create, Edit, Delete files

Disk quota of 2 GB per user

screenshots
