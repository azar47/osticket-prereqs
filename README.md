<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.


## Environments and Technologies Used
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used
- Windows 10 (21H2)

## List of Prerequisites
- IIS Installed with CGI enabled  
- PHP Manager for IIS  
- URL Rewrite Module  
- PHP 7.3.8  
- MySQL 5.5.62  

## Installation Steps

![ost-prereq ss1](https://github.com/user-attachments/assets/2458c466-829c-439b-bcc2-e17ade76cedf)
Azure Windows 10 VM created and accessed through Remote Desktop.

### *(Screenshot 2 here)*
IIS installed with Application Development Features and CGI enabled.

### *(Screenshot 3 here)*
IIS with CGI, URL Rewrite, and PHP Manager installed.

### *(Screenshot 4 here)*
osTicket files placed in 'C:\inetpub\wwwroot' and site loaded in browser.

### *(Screenshot 5 here)*
Required PHP extensions enabled in IIS (imap, intl, opcache).

### *(Screenshot 6 here)*
MySQL installed and the 'osTicket' database created using HeidiSQL.

### *(Screenshot 7 here)*
osTicket installation completed and the Admin login page accessible.

