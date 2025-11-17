<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.

## Video Demonstration
YouTube: How To Install osTicket with Prerequisites

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

### *(Screenshot 1 here)*
Azure Windows 10 VM created and accessed through Remote Desktop.

### *(Screenshot 2 here)*
IIS installed with Application Development Features and CGI enabled.

### *(Screenshot 3 here)*
PHP registered inside IIS (using PHP Manager).

### *(Screenshot 4 here)*
osTicket files placed in `C:\inetpub\wwwroot` and site loaded in browser.

### *(Screenshot 5 here)*
Required PHP extensions enabled in IIS (imap, intl, opcache).

### *(Screenshot 6 here)*
MySQL installed and the `osTicket` database created using HeidiSQL.

### *(Screenshot 7 here)*
osTicket installation completed and the Admin login page accessible.

