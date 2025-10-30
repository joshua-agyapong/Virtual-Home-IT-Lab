# Virtual-Home-IT-Lab
# 🧩 Home IT Help Desk Lab

## Overview
This project builds a small virtual IT environment using **VirtualBox**, **Windows Server 2022**, and **Windows 10**.  
It simulates how an entry-level IT professional supports users, manages Active Directory, and handles network tasks.

---

## 🧱 Module 1 – Virtual Environment Setup

**Reason:** Create an isolated virtual network to safely learn IT administration.  
**Action:**
1. Installed VirtualBox 7.x on Windows 11 host.  
2. Downloaded Windows Server 2022 and Windows 10 ISOs.  
3. Created VM folder and ISO library at `C:\ISOs\`.  
4. Built the first virtual machine (DC01) with:
   - 4 GB RAM
   - 100 GB dynamically allocated disk  
   - Bridged or Host-Only Adapter (since “Internal Network” unavailable)
5. Attached Windows Server 2022 ISO.

**Result:**  
Virtual machine boots from ISO and starts Windows Server setup.

**Skills Learned:**  
Virtualization basics, virtual disk management, ISO mounting.

📸 `/Screenshots/VBox_Install.png`  
📸 `/Screenshots/DC01_Storage_Config.png`  
📸 `/Screenshots/DC01_Network_Config.png`

---

## ⚙️ Module 2 – Install Windows Server 2022

**Reason:** Prepare a base server OS for domain configuration.  
**Action:**
1. Booted from Server 2022 ISO.  
2. Installed **Windows Server Datacenter (Desktop Experience)**.  
3. Created password for the built-in Administrator account.  
4. Logged in and confirmed Server Manager launched.

**Result:**  
Windows Server installed successfully and ready for configuration.

**Skills Learned:**  
Operating system installation, administrative login.

📸 `/Screenshots/DC01_FirstLogin.png`

---

## 🌐 Module 3 – Server Configuration

**Reason:** Make server identifiable and reachable in network.  
**Action:**
1. Renamed computer to **DC01**.  
2. Set static IP address:  
