<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Virtual Machine in Microsoft Azure
- Download and Install osTicket Setup Files (Source: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 )
- Download and Install Heidi SQL (Source: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 )

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/QoslDMQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Create a Resource Group in Microsoft Azure. Name your Resource Group "osTicket" and then select the region you desire. In this case, I chose (US) West US 3. Note: Remember to select the same region for your Virtual Machine to avoid errors.
</p>
<br />

<p>
<img src="https://i.imgur.com/vN8mfOj.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Create a Virtual Machine. Click the dropdown arrow for resource group and select "osTicket". Name your Virtual Machine "Vm-osticket". Reminder: Ensure your region matches the one in your Resource Group. Select Windows 10 Pro for the image. Select a VM with 2-4 Virtual CPUs to avoid lag while in use. Username: labuser (for example/whatever you chose)
Password: osTicketPassword1! (for example/whatever you chose)
</p>
<br />

<p>
<img src="https://i.imgur.com/paqDdrh.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Ensure you check the box for Licensing to avoid errors when creating your VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/9wl1yOC.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Click on Control Panel -> Programs -> Programs and Features. Select "Turn Windows Features on or off". Then click on "+" sign next to World Wide Web Services -> Application Development Features -> [X] CGI.
</p>
<br />

<p>
<img src="https://i.imgur.com/AWI91ye.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Download PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/85dvUTU.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Install PHP Manager for IIS. (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/7OqKrGS.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Download Rewrite Module. (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/56ZhRPr.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Install Rewrite Module. (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/RSpigiI.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Create a new file in C drive.
</p>
<br />

<p>
<img src="https://i.imgur.com/b9FjDag.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
9a. Create the directory C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/RF5GvGh.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/khGtLqP.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. If prompted during PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) download, select "keep anyway".
</p>
<br />

<p>
<img src="https://i.imgur.com/N1KivAr.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Download VC_redist.x86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/zOF8sT7.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
12a. Install VC_redist.x86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/st8rZ1u.png" height="90%" width="90%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Download MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/uBux3lh.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13a. Install MySQL 5.5.62 (mysql-5.5.62-win32.msi) 
</p>
<br />

<p>
<img src="https://i.imgur.com/DRDuLIF.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13b. Select "Typical" setup.
</p>
<br />

<p>
<img src="https://i.imgur.com/Tm5c0wc.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13c. Launch MySQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/5ATb9dF.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13d. After launch, select "Standard Configuration" then click next.
</p>
<br />

<p>
<img src="https://i.imgur.com/kCWswjm.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13e. Check the box for "Launch MySQL Server automatically" then select next.
</p>
<br />

<p>
<img src="https://i.imgur.com/mFDykor.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
13f. Enter root password as "Password1". Select next. Note: Remember username is root, password is Password1.
</p>
<br />

<p>
<img src="https://i.imgur.com/0h7BNDQ.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Open IIS as an Admin.
</p>
<br />

<p>
<img src="https://i.imgur.com/9DNazM3.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/f9s26f5.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/s4SFB8o.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. Register PHP from within IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/ECTS1Tf.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/8mZP9KC.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. Download osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/8X3MtiD.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
17a. Extract and copy “upload” folder to c:\inetpub\wwwroot
</p>
<br />

<p>
<img src="https://i.imgur.com/HD9uoAr.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
17b. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/ECTS1Tf.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>
<img src="https://i.imgur.com/ujesVxx.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
19. Go to sites -> Default -> osTicket. On the right, click “Browse *:80”

</p>
<br />

<p>
<img src="https://i.imgur.com/NasetgE.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hlqU7VG.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DDwgeSt.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jdg43db.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
20. Note that some extensions are not enabled. Go back to IIS, sites -> Default -> osTicket. Double-click PHP Manager. Click “Enable or disable an extension”, Enable: php_imap.dll, Enable: php_intl.dll., Enable: php_opcache.dll., Refresh the osTicket site in your browse, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/zWgFpDi.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/I6uTqaq.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
21. Rename: ost-config.php, From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/Nv8uN1P.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/dTeuPQe.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/rScllfb.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/K45lqu5.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/C2nNkUk.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/WljbBmx.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/LPkzidY.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2osoUhU.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
</p>
<p>
22. Assign Permissions: ost-config.php, Disable inheritance -> Remove All, New Permissions -> Everyone -> All
</p>
<br />

<p>
<img src="https://i.imgur.com/jdg43db.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2LI96UQ.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<p>
NOTE: INFORMATION CAN BE DIFFERENT THAN MINE AS I HAVE ENCOUNTERED ERRORS AT THE END. REMEMBER TO PUT DIFFERENT EMAIL ADDRESSES AND NOT USE ADMIN AS A USERNAME. 
</p>
<img src="https://i.imgur.com/jdg43db.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
23. Continue Setting up osTicket in the browser (click Continue), Name Helpdesk, Default email (receives email from customers). Note: Remember to write down login information on notepad (For practice only). WARNING: DO NOT CLICK "INSTALL NOW" YET UNTIL HEIDI SQL IS INSTALLED.
</p>
<br />

<p>
<img src="https://i.imgur.com/Bbp13Q9.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xV9KX4N.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<p>
Keep clicking next.
</p>
<img src="https://i.imgur.com/2tg1nlP.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/bGwpunq.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/PfRbZA4.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/gSDx4tR.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/7aSz60Q.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/3R5uBJF.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
24. From the Installation Files, download and install HeidiSQL. Open Heidi SQL. Create a new session, root/Password1, Connect to the session, Create a database called “osTicket”.
</p>
<br />

<p>
<img src="https://i.imgur.com/hWeO1wk.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
25. Continue Setting up osticket in the browser, MySQL Database: osTicket, MySQL Username: root, MySQL Password: Password1, Click “Install Now!”
</p>
<br />

<p>
<img src="https://i.imgur.com/EhTqYpM.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yFcYRpL.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
26. Congratulations, hopefully it is installed with no errors! Browse to your help desk login page: http://localhost/osTicket/scp/login.php NOTE: I DID ENCOUNTER A COUPLE ERRORS DUE TO A BAD USERNAME AND CONFLICTING EMAILS. CHANGED USERNAME FROM ADMIN TO EXAMPLE. CHANGED USER EMAIL TO EXAMPLE@HELPER.COM SO IT WON'T CONFLICT WITH THE DEFAULT EMAIL ADDRESS.
</p>
<br />

<p>
<img src="https://i.imgur.com/8aXqchj.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
27. End Users osTicket URL: http://localhost/osTicket/ 
</p>
<br />

<p>
<img src="https://i.imgur.com/eqX0YEp.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DHQdtkk.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iXlgXva.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yKbho4H.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
28. Clean up, Delete: C:\inetpub\wwwroot\osTicket\setup, Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php, Notes: Browse to your help desk login page: http://localhost/osTicket/scp/login.php , End Users osTicket URL: http://localhost/osTicket/ 
</p>
<br />
