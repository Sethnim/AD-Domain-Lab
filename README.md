# Active Directory Domain Lab (Server 2022 + Windows 10 Client)

## Project Overview
This project demonstrates the setup of an **Active Directory (AD) environment** with Windows Server 2022 as a Domain Controller and a Windows 10 client joined to the domain.  
It also includes **DNS, OUs, Users/Groups, Shared Folders with NTFS permissions, and Group Policies (GPOs)** for security and customization.

Two members collaborated on this project to simulate a small enterprise IT infrastructure.

---

## Features Implemented
1. **Active Directory Setup**
   - Installed AD DS and configured DNS.
   - Promoted server to Domain Controller: `testdomain.local`.

2. **Client Domain Join**
   - Joined Windows 10 client to `testdomain.local`.
   - Configured DNS to `10.0.2.15`.

3. **Organizational Units (OUs) & Users/Groups**
   - Created OUs: `branch1` and `branch2`.
   - Created security groups: `IT_Admins` (branch1) and `HR_Admins` (branch2).
   - Added users:  
     - `john.it` → `IT_Admins`  
     - `alice.hr` → `HR_Admins`

4. **Shared Folders & Network Drive Mapping**
   - Created secure folders:
     - `C:\Sharedata\HR_Admin` → accessible only to `HR_Admins`.
     - `C:\Sharedata\IT_Admin` → accessible only to `IT_Admins`.
   - Network drives mapped:
     - `L:\` → `\\10.0.2.15\HR_Admin`
     - `M:\` → `\\10.0.2.15\IT_Admin`

5. **Group Policy (GPO)**
   - Disabled CMD for all users in the `HR_Admins` group.
   - Applied custom wallpaper for users in the `IT_Admins` group.

6. **Testing**
   - Verified domain login for users.
   - Confirmed GPO effects: CMD disabled (HR users) and wallpaper changed (IT users).

---

## Tools & Technologies Used
- **VirtualBox** – Virtualization
- **Windows Server 2022** – Domain Controller, AD DS, DNS, GPO, File Server
- **Windows 10** – Domain Client
- **Active Directory Users and Computers (ADUC)**
- **Group Policy Management (GPMC)**

---

## Screenshots
Screenshots of each step are included in the `screenshots/` folder:

- AD Installation & DNS Configuration  
- OU & Users/Groups Creation  
- Client Domain Join  
- Shared Folder & Network Drive Access  
- GPO Configuration (CMD Disable & Wallpaper)  
- Policy Enforcement Results  

---

## Learning Outcomes
Through this project, we gained hands-on experience in:
- Configuring and managing **Active Directory**.
- Implementing **OUs, Users, and Security Groups**.
- Setting **NTFS permissions** and **network shares**.
- Applying **Group Policies** for security and customization.
- Testing and troubleshooting domain environments.

---

## 👥Contributors
- **Member 1:** [P.D. Sethnim Dilneth]  
- **Member 2:** [S. Yathurshan]  

Both members implemented, tested, and documented different parts of the lab setup.

---

## 📌 How to Use
1. Clone the repository:  
   ```bash
   git clone https://github.com/Sethnim/AD-Domain-Lab.git
