# 🐧 Project 1: Building & Configuring a Linux Environment (Ubuntu on VirtualBox)

**Student:** Pelumi Johnson  
**Course:** Introduction to Linux  
**Submission Date:** 11/11/2025  

📄 **Full Lab Report:**  
👉 [Click here to open the complete lab report](https://github.com/Pelumi-Johnson/Building-Configuring-a-Linux-Environment/blob/main/Project%201%20(3).docx.pdf)

---

## 🌿 Overview
This project documents my first complete Linux environment build using **Ubuntu 24.04.3 LTS** inside **Oracle VirtualBox**. I installed the OS, verified network connectivity, explored the Linux file system, practiced file/directory management, created hard & symbolic links, managed users/groups, adjusted permissions, and installed/uninstalled packages using `apt`.

Linux feels like learning a workshop every command is a tool, every directory is a room, and wisdom comes by doing.

---

## 🎯 Objectives
- Set up a Linux virtual machine successfully
- Verify installation and internet connectivity
- Navigate the Linux file system with core commands
- Create, rename, delete files/directories
- Understand and create **hard links** vs **symbolic links**
- Create users/groups and manage membership
- Modify file permissions responsibly
- Install and remove packages with `apt`

---

## 🧰 Environment & Tools
- **Host Tool:** Oracle VirtualBox  
- **Guest OS:** Ubuntu 24.04.3 LTS  
- **VM Settings Used:**
  - **RAM:** 2 GB
  - **Storage:** 25 GB virtual hard drive
- **Install Options:**
  - Interactive installation
  - Language: English
  - Installation type: *Erase disk and install Ubuntu* (inside VM)
  - Enabled third-party software
  - Default app set
  - Created user account: **“Pelumi Johnson”**

---

## ✅ Part 1: Virtual Machine Setup & OS Installation

### 1.1 Create the Virtual Machine
Steps completed:
- Created a new VM in VirtualBox
- Allocated **2 GB RAM** and **25 GB disk**
- Attached the **Ubuntu ISO**
- Started installation using interactive setup

### 1.2 Install Ubuntu 24.04.3 LTS
- Chose English language
- Selected default installation options
- Enabled third-party software
- Created the user account and completed installation
- Rebooted VM into Ubuntu successfully

---

## 🌐 Part 1.4: Verify Installation (Network Test)

### Command Used
```bash
ping google.com
```

## 🌐 Network Connectivity Verification

### Purpose
Tests internet connectivity by sending packets to an external host and checking for replies.

### Result
Received repeated replies like:
```
64 bytes from google.com...
```
✅ This confirmed the OS was installed correctly and the VM had working network access.

### Screenshot Placeholder
assets/screenshots/ping-google.png

---

## 📁 Part 2: File System Exploration

### 2.1 Navigating the File System

#### Commands Practiced
```
pwd
ls
cd
```

#### What They Do
- `pwd` → prints the current directory path  
- `ls` → lists files/folders in the current directory  
- `cd` → changes directories  

#### Key Directories Explored
- `/home` → user files and personal directories  
- `/var` → logs and variable system data  
- `/etc` → system and application configuration files  

#### Screenshot Placeholders
assets/screenshots/pwd-ls.png  
assets/screenshots/etc-var-home.png  

---

### 2.2 Creating & Manipulating Files and Directories

#### Commands Used
```
mkdir project1_files
cd project1_files
touch file1.txt
mv file1.txt renamed_file.txt
rm renamed_file.txt
```

#### What This Reinforced
- How to create directories and files  
- How to rename files safely  
- How to remove files intentionally (with care)  

#### Screenshot Placeholder
assets/screenshots/file-create-rename-delete.png  

---

### 2.3 Creating Links (Hard vs Symbolic)

#### Hard Link
- Direct link to the file’s data (inode)  
- Still works even if the original filename is deleted  

**Command**
```
ln file1.txt file1_hardlink.txt
```

#### Symbolic Link (Symlink)
- Shortcut pointing to a file path  
- Breaks if the original file is removed or moved  

**Command**
```
ln -s file1.txt file1_symlink.txt
```

#### Screenshot Placeholder
assets/screenshots/hardlink-symlink.png  

---

## 👥 Part 3: User & Group Management

### 3.1 Create New Users and Groups

#### Commands Used
```
sudo useradd student1
sudo passwd student1
sudo groupadd project1_group
sudo usermod -aG project1_group student1
```

#### Notes
- `useradd` creates the account (no output if successful)  
- `passwd` prompts for password creation  
- `groupadd` creates the group (no output if successful)  
- `usermod -aG` adds the user to the group (no output if successful)  

#### Screenshot Placeholder
assets/screenshots/user-group-setup.png  

---

## 🔐 Part 3.2: File Permissions

### Commands Used
```
chmod u+rw permissions_test.txt
chmod o-w permissions_test.txt
```

### Meaning
- `chmod u+rw` → gives the owner read + write permissions  
- `chmod o-w` → removes write permission from “others”  

### Screenshot Placeholder
assets/screenshots/permissions-chmod.png  

---

## 📦 Part 4: Package Management (APT)

### 4.1 Install a Package

#### Commands Used
```
sudo apt update
sudo apt install curl
curl --version
```

#### Purpose
- `apt update` refreshes package lists  
- `apt install curl` installs curl  
- `curl --version` verifies installation  

#### Screenshot Placeholder
assets/screenshots/curl-install-version.png  

---

### 4.2 Uninstall a Package

#### Command Used
```
sudo apt remove curl
```

#### Result
curl was uninstalled from the system successfully.

#### Screenshot Placeholder
assets/screenshots/curl-remove.png  

---

## 🧾 Conclusion (Reflection)

### ✅ What I Learned
- How to install Ubuntu using VirtualBox  
- How to use Linux terminal commands with growing confidence  
- How to manage files, users, groups, permissions, and packages  

### 🧱 Challenges Encountered
- Experienced setup and boot errors during installation  
- Resolved issues by restarting, recreating the VM, and following steps carefully  

### 🌱 Future Considerations
- Continue strengthening Linux skills  
- Explore deeper system administration tasks  
- Grow in managing and securing Linux systems  

---

## 📚 References
- Ubuntu Documentation: https://ubuntu.com/tutorials  
- Oracle VirtualBox User Manual: https://www.virtualbox.org/manual/UserManual.html

---

## ⭐ Quick Copy: Commands Recap

### Verify Connectivity
```
ping google.com
```

### Navigate
```
pwd
ls
cd /home
cd /var
cd /etc
```

### Files & Directories
```
mkdir project1_files
cd project1_files
touch file1.txt
mv file1.txt renamed_file.txt
rm renamed_file.txt
```

### Links
```
ln file1.txt file1_hardlink.txt
ln -s file1.txt file1_symlink.txt
```

### Users & Groups
```
sudo useradd student1
sudo passwd student1
sudo groupadd project1_group
sudo usermod -aG project1_group student1
```

### Permissions
```
chmod u+rw permissions_test.txt
chmod o-w permissions_test.txt
```

### Packages
```
sudo apt update
sudo apt install curl
curl --version
sudo apt remove curl
```
