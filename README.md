# Active Directory Corporate Network Simulation

## 📖 Objective

In this lab, I am taking a step ahead and upgrade the active directory home lab into a corporate network where I can implement security practices. I am going to be using the applications that comes pre-installed with Windows Active Directory and install/configure secure connectivity/networking solutions (OpenSSH and OpenVPN).

## Table of Contents:

1. [NTFS](#-NTFS)
2. [Group Policy Management](#-Group-Policy-Management)
3. [Firewall Rules](#-Firewall-Rules)
4. [DNS Proxy](#-DNS-Proxy)
5. [OpenSSH Server](#-OpenSSH-Server) 
6. [Windows Server Update Services](#-Windows-Server-Update-Services)
7. [OpenVPN Access Server](#-OpenVPN-Access-Server)


_____________________________________________________________________________________________________________________________________________________________________________________________________________________

## 📁 NTFS

  ![image](https://github.com/user-attachments/assets/c2a15292-a52f-4d7c-a547-d1859f548877)  ![image](https://github.com/user-attachments/assets/e31751de-caf6-4764-aed9-43d32804f9ea)


I ran dsa.msc to manage Active Directory Users and Computers (ADUC) for users accounts, groups, and organizational units (OUs). I selected full control of permissions for the admin and use least privilege for the different departments and users. 

## 📑 Group Policy Management

```cmd
net accounts /minpwlen:8  #minimum password length
net accounts /maxpwage:90 #maxium password age            
net accounts /minpwage:1  #minimum password age            
net accounts /uniquepw:10 #the last ten unique passwords used
```

I updated the Password Policy using the Command Prompt (Terminal) such as modifying the minimum password length, password complexity, maximum password age, minimum password age, and enforce password history. 


![prevent usb storage devices](https://github.com/user-attachments/assets/c8ba6c64-70d9-40a7-a3f2-23bbb16efc94)

Additionally, I configured the Removable Storage Access to prevent access to USB drives. After the Group Policy Management has been configured, I then apply the updates in an instance for these configurations.

```cmd
gpupdate / force
```

## 🧱 Firewall Rules

I ran wf.msc to apply firewall rules for Inbound/Outbound traffic using Microsoft Defender Firewall. The rules I applied for the firewall is specifically for DNS (Inbound/Outbound). 

- Created a new rule (Inbound/Outbound) from the Inbound Rules or Outbound Rules
- Specified the port 53 (UDP)
- Allow the connection if it is secure
- For Inbound, I selected Domain and Private
- For Outbound, I selected all profiles (Domain, Private, and Public)
- I keep everything else as default and created the rules

![image](https://github.com/user-attachments/assets/680bfcc9-9128-452e-9d76-2c1092f13659)  ![image](https://github.com/user-attachments/assets/f97714ff-0f03-490e-bec0-05754d70cb36)

## 📱 DNS Proxy

![image](https://github.com/user-attachments/assets/305506bf-1317-40c7-bcbe-bc1b22b11675)

![image](https://github.com/user-attachments/assets/79bfb84a-d59e-44a5-99e6-2d905ab14376)

## 🐚 OpenSSH Server

Configuring OpenSSH Server for Secure File Transfer Protocol (SFTP)


## 🗄️ Windows Server Update Services

Configuring WSUS for users to have automatic updates and patch management available. 

## 🔐 OpenVPN Access Server

Configuring OpenVPN Access Server  

