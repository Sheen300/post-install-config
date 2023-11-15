<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Step 1: Go inside portal.azure.com and click on Virtual Machines. Select the virtual machine that was created and copy the Public IP address. Open remote desktop from the Start memu. Create a new connection by copying the IP address into remote desktop.
- Step 2: Click Start. Control panel. Programs. Click Turn Windows features on or off. Internet formation services. Application development features. Check CGI. Common http features. Check every box. Click OK. Close when completed. To test that it has worked. Go to a web browser and type the following: 127.0.0.1. This image should have appeared if it was done correctly.

- ![image](https://github.com/Sheen300/post-install-config/assets/150862861/d7a7bf4a-b034-4486-a12d-6a195b26b450)

- Step 3: There have been installation files given for PHP Manager and Rewrite Modules. Download them in a new tab. 
- Step 4: Download PHP 7.3.8. and unzip the contents into the C drive. Go to C drive. Right-click. Click New. Folder. Type PHP. Done.
- Step 5: From installation list, download PHP zip. Click on the 3 dots when it's finished and click "Keep". Go to downloads. Right-click on PHP. Click Extract all. Click browse. This PC. C drive. PHP . Extract. 

<h2>Configuration Steps</h2>

- Step 6. Click and download VC Redist installation link. Complete the same steps for MySQL 5.5.62. Click it, complete the download.
- Step 7. Go to MySQL 5.5.62. Click it to complete the download. Select Typical. Standard configuration. Click Next. The "root" is your username. Password will be "Password1" for simplicity.

- Step 8. Click on Start. Type IIS. Right click it and run as an administrator. Click PHP Manager. Register new PHP version. C. drive. PHP. php-cgi. Click OK. Click name of the web serve. Click on Restart.

- Step 9. Download osTicket from the installation files.
- Step 10. Go back to IIS. vm-osTicket. Sites. Default Web Site. osTicket. On the right, click Browse *80. The following screen should appear.

- ![image](https://github.com/Sheen300/post-install-config/assets/150862861/bf82200e-9d89-4ce0-a01d-589edbc6b510)

- Step 11. Now we will enable extensions within osTicket. Go back to IIS. Sites. Default ticket. Double-click PHP Manager. Enable or disable an extension. Enable the following: php_imap.dll. php_intl.dll. php.opcache.dll. Your view on the osTicket web page should change from this:
-
- ![image](https://github.com/Sheen300/post-install-config/assets/150862861/5fb58632-9820-4e06-bff6-fc44027367e9)

 To this: 

 - ![image](https://github.com/Sheen300/post-install-config/assets/150862861/6856662d-e1a5-43ef-938c-e9e6cdf9c262)

- Step 12: Go back to C drive. wwwroot. Click osTicket. Click include. Change ost-sameconfig folder name to now just ost-config. Right-click. Properties. Security. Advanced. Disable inheritance. Remove all permissions. Click Add. Select a principal. Type everyone. Apply. Click OK. Click OK.

- Step 13: Go back to osTicket in the browser. Continue setting up a user in the osTicket.
- Step 14: Download and install HeidiSQL. Launch. Click New. Username is root. Password is whatever you chose.
- Step 15: On the osTicket web page. Enter your root name and password for Heidi SQL.
- Step 16: Go back to Heidi. Go to unnamed. Right-click. Create New. Database. Name it osTicket. You should see this.

- ![image](https://github.com/Sheen300/post-install-config/assets/150862861/543bb079-3b8a-401e-86db-ca29da3ba48d)

- Step 17: Go back to osTicket web page. Enter osTicket in the "My SQL Database" space. Should be able to Install Now. You should see this on the web page now.

- ![image](https://github.com/Sheen300/post-install-config/assets/150862861/e3986f97-1d83-4c6c-816d-129c35269cc3)

- DONE!!

- To clean up. Go back to This PC. C drive. inetpub. wwwroot. osTicket. "Setup" folder. Delete.
