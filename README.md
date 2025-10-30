# 🧩 Windows Server 2022 Home Lab – Active Directory Domain Setup

### 🎯 Objective
Build a self-contained Windows Server 2022 lab in VirtualBox to simulate a small company IT environment.  
Configured networking, static IP, and installed Active Directory Domain Services (AD DS) with Group Policy Management.

---

## 🖥️ Environment Setup

| Component | Details |
|------------|----------|
| **Hypervisor** | Oracle VirtualBox 7.2.4 |
| **VM Name** | DC01 (or LAB-SRV01) |
| **OS** | Windows Server 2022 Datacenter |
| **Disk Size** | 100 GB (VDI) |
| **Network Mode** | Bridged Adapter |
| **RAM** | 4 GB |
| **CPU Cores** | 2 |

---

## 🧱 Module 1 – Virtual Machine Creation

**Reason:** Set up a dedicated server for identity management practice.  
**Action:** Created a new VM, attached Windows Server ISO, and configured storage/network.  
**Result:** Windows Server 2022 successfully installed in VirtualBox.  
**Skills Learned:** VM provisioning, ISO management, VirtualBox configuration.

📸 `Screenshots/DC01_FirstLogin.png`

---

## 🧩 Module 2 – Server Configuration

**Reason:** Establish a consistent environment for networking and identity roles.  
**Action:** Renamed server to `LAB-SRV01` and assigned a static IP.  
**Result:** Server reachable by a fixed IP address and easily identifiable in the lab.  
**Skills Learned:** Computer renaming, IPv4 setup, static addressing.

📸 `Screenshots/DC01_Rename.png`  
📸 `Screenshots/DC01_StaticIP.png`

---

## 🧩 Module 3 – AD DS Installation

**Reason:** Install Active Directory for centralized authentication and user management.  
**Action:** Used *Add Roles and Features Wizard* to install:  
- Active Directory Domain Services  
- Group Policy Management  
- .NET Framework 3.5 / 4.8  

**Result:** AD DS role installed successfully and ready for promotion.  
**Skills Learned:** Role-based installation, feature selection, dependency management.

📸 `Screenshots/DC01_RoleBasedInstall.png`  
📸 `Screenshots/DC01_ADDS_Features.png`  
📸 `Screenshots/DC01_ADDSInstallConfirm.png`

---

## 🧩 Module 4 – Domain Promotion

**Reason:** Convert the standalone server into a domain controller.  
**Action:** Promoted LAB-SRV01 to a new forest domain `techlab.local`.  
**Result:** Domain successfully created and verified login as `TECHLAB\Administrator`.  
**Skills Learned:** Forest creation, DNS setup, domain promotion, DSRM configuration.

📸 `Screenshots/DC01_DomainLogin.png`

---

## 🧰 Tools Used

- Oracle VirtualBox  
- Windows Server 2022 ISO  
- Server Manager (Add Roles and Features Wizard)  
- Group Policy Management Console  

---

## 🧠 Key Takeaways

- Learned how to deploy Windows Server from scratch.  
- Practiced static IP and DNS configuration.  
- Built a functional domain controller in a home lab environment.  
- Gained real-world familiarity with IT helpdesk and systems administration tasks.

---

## 🧾 Notes
All installation steps and credentials are documented in `/Notes/SetupSteps.txt`  
Default admin password: `P@ssword123!`

---

## 🧩 Next Phase
**Upcoming modules:**
- Create Organizational Units (OUs)
- Add domain users and groups  
- Apply and test Group Policy Objects (GPOs)  
- Join a Windows 10 client to the domain  
