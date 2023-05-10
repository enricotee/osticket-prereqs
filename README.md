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
<img src="https://i.imgur.com/QoslDMQ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
