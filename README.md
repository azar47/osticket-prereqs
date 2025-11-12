# osTicket - Prerequisites and Installation

This repository provides a complete guide for installing the open-source help desk ticketing system **osTicket** on a Windows 10 Azure Virtual Machine using IIS, PHP, and MySQL.

---

## Environments and Technologies Used

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Protocol (RDP)
- Internet Information Services (IIS)
- PHP 7.3.8
- MySQL 5.5.62
- HeidiSQL (for database management)

---

## Operating Systems Used

- Windows 10 (21H2)

---

## List of Prerequisites

- Azure Virtual Machine (Windows 10, 4 vCPUs)  
- IIS installed with CGI enabled  
- PHP Manager for IIS  
- PHP 7.3.8  
- MySQL 5.5.62  
- VC++ Redistributable (VC_redist.x86.exe)  
- IIS Rewrite Module  
- HeidiSQL (optional, for database management)

---

## Installation Steps

### 1. Create Azure Virtual Machine

- Name: `osticket-vm`  
- Username: `labuser`  
- Password: `osTicketPassword1!`  
- OS: Windows 10, 21H2  
- vCPUs: 4  

Log into the VM via Remote Desktop once it is created.

---

### 2. Prepare Installation Files

- Download `osTicket-Installation-Files.zip` to the desktop  
- Unzip to `C:\Users\labuser\Desktop\osTicket-Installation-Files`  
- This folder contains osTicket, PHP, MySQL, and required dependencies.

---

### 3. Install IIS and Enable CGI

- Control Panel → Programs → Turn Windows features on or off  
- Internet Information Services → World Wide Web Services → Application Development Features → check **CGI**  
- Click OK and wait for IIS to install.

---

### 4. Install Required Dependencies

From the “osTicket-Installation-Files” folder:

1. PHP Manager for IIS (`PHPManagerForIIS_V1.5.0.msi`)  
2. IIS Rewrite Module (`rewrite_amd64_en-US.msi`)  
3. VC++ Redistributable (`VC_redist.x86.exe`)  
4. MySQL 5.5.62 (`mysql-5.5.62-win32.msi`)  
   - Typical Setup → Standard Configuration  
   - Root Username: `root`  
   - Password: `root`  
   - Launch Configuration Wizard after installation  

---

### 5. Setup PHP

1. Create directory: `C:\PHP`  
2. Unzip PHP 7.3.8 (`php-7.3.8-nts-Win32-VC15-x86.zip`) into `C:\PHP`  
3. Open IIS as Administrator → PHP Manager → Register new PHP version → select `C:\PHP\php-cgi.exe`  
4. Reload IIS (Stop and Start the server)

---

### 6. Install osTicket

1. Unzip `osTicket-v1.15.8.zip`  
2. Copy the `upload` folder to `C:\inetpub\wwwroot`  
3. Rename `upload` → `osTicket`  
4. Reload IIS (Stop and Start the server)  
5. Open browser → Sites → Default Web Site → osTicket → Browse `*:80`

---

### 7. Enable PHP Extensions

- Open PHP Manager in IIS  
- Click “Enable or disable an extension”  
- Enable: `php_imap.dll`, `php_intl.dll`, `php_opcache.dll`  
- Refresh the osTicket site in your browser.

---

### 8. Configure osTicket

1. Rename `C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php` → `ost-config.php`  
2. Assign Permissions for `ost-config.php`:  
   - Disable inheritance → Remove all  
   - Add: Everyone → Full Control

---

### 9. Setup MySQL Database

1. Install and open **HeidiSQL**  
2. Create a new session → Connect with MySQL `root/root`  
3. Create a new database named `osTicket`

---

### 10. Complete osTicket Installation in Browser

1. Go to osTicket web setup page  
2. Fill out required fields:  
   - Helpdesk Name: `Helpdesk`  
   - Admin Email: your default email  
3. Database Settings:  
   - Database Name: `osTicket`  
   - Username: `root`  
   - Password: `root`  
4. Click **Install Now!**

---

### 11. Post-Installation Cleanup

- Delete `C:\inetpub\wwwroot\osTicket\setup` folder  
- Set `ost-config.php` permissions → Read-only

---

## Access URLs

- **Admin Login:** [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)  
- **End User Access:** [http://localhost/osTicket/](http://localhost/osTicket/)

---

## Congratulations!

osTicket has been successfully installed and configured. You can now log in as an admin to start managing tickets, departments, and user accounts.
