<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket Logo" />
</p>

# osTicket – Prerequisites and Installation

## Project Summary
In this project, I installed and prepared **osTicket**, an open-source help desk ticketing system, on a **Windows 10 virtual machine** running in **Microsoft Azure**.  
The project covers installing required components such as **IIS**, **PHP**, **MySQL**, and completing the initial osTicket setup in the browser.

**Environments Used:** Azure Virtual Machine, Remote Desktop  
**Operating System:** Windows 10  
**Technologies / Tools:** IIS, PHP Manager, URL Rewrite Module, PHP 7.3.8, MySQL 5.5.62, HeidiSQL, osTicket v1.15.8

---

## Media

(Add your screenshots in this section)

**Screenshot 1:** Azure VM running Windows 10.  
**Screenshot 2:** IIS installed with CGI enabled.  
**Screenshot 3:** PHP registered in IIS.  
**Screenshot 4:** osTicket folder inside 'wwwroot' and the site loading in browser.  
**Screenshot 5:** MySQL database created in HeidiSQL.  
**Screenshot 6:** osTicket installation successful (Admin login page).  

---

## Demonstration
1. Created a Windows 10 VM in Azure and logged in using Remote Desktop.  
2. Installed IIS and enabled the required web features.  
3. Installed PHP Manager, URL Rewrite, PHP 7.3.8, and configured PHP inside IIS.  
4. Installed MySQL and created an 'osTicket' database using HeidiSQL.  
5. Copied the osTicket files into 'C:\inetpub\wwwroot' and ran the web installer.  
6. Completed the setup and verified access to both:  
   - Admin Panel: 'http://localhost/osTicket/scp/login.php'
   - End-User Portal: 'http://localhost/osTicket/'

This project demonstrates deploying a help desk ticketing system and configuring the required web and database components in a cloud environment.
