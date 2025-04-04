# ■ Active Directory Basics 

## ■ Objective  
This room introduced the core components of Active Directory and how it's used to manage users, computers, and security policies in enterprise Windows environments. The goal was to get hands-on experience with domain structures, user/computer objects, OUs, delegation, and GPOs.

## ■ Tools & Techniques Used  
- **Remote Desktop Protocol (RDP)** – Logged in as different domain users  
- **Active Directory Users and Computers** – Created, modified, and deleted users and OUs  
- **PowerShell** – Used `Set-ADAccountPassword` and `Set-ADUser` for password resets  
- **Group Policy Management** – Created and linked GPOs for password policies and control panel restrictions  
- **Command Line (Windows)** – Ran `gpupdate /force` to push GPOs manually  

## ■ Key Findings / Evidence  
| Action / Indicator                   | Description                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------|
| Domain Admin Group                  | Manages all domain resources                                               |
| Machine Account Format              | `COMPUTERNAME$` (e.g., `TOM-PC$`)                                          |
| OU Creation                         | Created separate OUs for Workstations, Servers, and Departments            |
| Delegation                          | Phillip delegated rights to reset passwords in specific OUs                |
| GPO Implementation                  | Enforced password length & auto-lock screen inactivity                     |
| Control Panel Restriction           | Blocked for non-IT users using user-targeted GPO                           |
| Kerberos & NetNTLM                  | Explored differences between authentication protocols                      |
| Trees, Forests, Trusts              | Learned how multi-domain structures are handled and connected              |
| Final Flag                          | `THM{thanks_for_contacting_support}` found on Sophie's desktop            |

## ■ Analysis Summary  
- Understood how Active Directory organizes and centralizes domain resources  
- Practiced managing users, computers, and OUs via GUI and PowerShell  
- Implemented basic but real-world GPO policies  
- Delegated admin control for better role-based access  
- Learned authentication protocol differences (Kerberos vs. NetNTLM)

## ■ Skills Demonstrated  
- Active Directory administration  
- User and machine object management  
- Organizational Unit
