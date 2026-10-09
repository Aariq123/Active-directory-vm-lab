# Active-directory-vm-lab

# Windows Server Active Directory Home Lab

## 📌 Project Overview
This project details the step-by-step deployment of an Active Directory (AD) environment built entirely within **Oracle VirtualBox**. Following foundational industry practices, I deployed a Windows Server instance, promoted it to a Domain Controller, established an organizational structure with users and groups, and successfully integrated a Windows client machine into the domain.

## 🛠️ Environment & Tools
* **Hypervisor:** VirtualBox
* **Domain Controller OS:** Windows Server (Standard / Evaluation)
* **Client OS:** Windows 10 / 11 Pro
* **Core Services:** Active Directory Domain Services (AD DS), DNS

---

## 🚀 Phase 1: Environment Setup
In this phase, I configured the virtualized environment and installed the base operating systems.
* Set up a dedicated virtual network in VirtualBox so the Server and Client could talk to each other safely.
* Installed the Windows Server operating system.

![VirtualBox Network Configuration](images/YOUR-IMAGE-NAME-HERE.png)
![Windows Server Base Installation](images/YOUR-IMAGE-NAME-HERE.png)

---

## 🌲 Phase 2: Forest Creation & Domain Controller Promotion
Here, I turned the standalone server into the central brain of the network—the **Domain Controller (DC)**.
* Installed the Active Directory Domain Services (AD DS) role.
* Promoted the server, which automatically created a new **Active Directory Forest** (the logical boundary for the network).

![AD DS Role Installation](images/YOUR-IMAGE-NAME-HERE.png)
![DC Promotion Wizard](images/YOUR-IMAGE-NAME-HERE.png)

---

## 👥 Phase 3: Organizational Units (OUs), Groups, and Users
To keep the company organized, I built a logical structure inside Active Directory Users and Computers (ADUC).
* **Organizational Units (OUs):** Think of these like folders to organize people and computers based on departments.
* **Security Groups:** Created three distinct groups to manage permissions efficiently: `Help Desk`, `IT Support`, and `Accounting`.
* **Users:** Created 3 individual employee user accounts and assigned them to their respective groups.

![OU Tree Structure](images/YOUR-IMAGE-NAME-HERE.png)
![Created Security Groups](images/YOUR-IMAGE-NAME-HERE.png)
![New User Account Creation](images/YOUR-IMAGE-NAME-HERE.png)

---

## 🔐 Phase 4: Client Integration, Delegation & Access Control
The final phase proved that the lab actually works by connecting a separate machine to our new domain.
* **Domain Join:** Changed the client machine's DNS settings to point to the Server, then joined it to the domain. The machine now safely appears in the DC's `Computers` container.
* **Authentication Testing:** Verified network access by logging in both as the powerful Domain Administrator and as one of our newly created standard users.
* **Delegation of Control:** Practiced the security principle of "least privilege" by delegating specific permissions (like resetting passwords) to the Help Desk/IT Support teams without making them full administrators.

![Client DNS Settings](images/YOUR-IMAGE-NAME-HERE.png)
![Successful Domain Join](images/YOUR-IMAGE-NAME-HERE.png)
![User Login Verification](images/YOUR-IMAGE-NAME-HERE.png)
![Delegation of Control Wizard](images/YOUR-IMAGE-NAME-HERE.png)
