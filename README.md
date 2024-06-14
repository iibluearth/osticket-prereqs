`# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Video Demonstration</h2>

 ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

 <h2>Environments and Technologies Used</h2>

 - Microsoft Azure (Virtual Machines/Compute)
 - Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Using 4 vCPU virtual machine through Microsoft Azure. 
- Download the necessary installation files through [Link 1](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) and [Link 2](https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe 
) 

 <h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/kXwcflr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/KxIUQmp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
1. Download Installation Files:

 - Log into the VM and download the installation files, resulting in one zip folder containing multiple files and one HeidiSQL installation file.
</p>
<br />

<p>
<img src="https://i.imgur.com/vwFvJu7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Open Control Panel:

- Search for "Control Panel" in the bottom left Windows search bar and click on it.
- Click on "Programs" within the Control Panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/rZCBFtT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/Xa6lbpN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Turn on Windows Features:

- Click on "Turn Windows features on or off" under "Programs and Features".
- Check "Internet Information Services" and expand its folders to select necessary features.
- Click "OK" to install and close the window once installation completes.
</p>
<br />

<p>
<img src="https://i.imgur.com/nwQtLD2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/dZuG7ci.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Create PHP Folder:

- Open File Explorer and navigate to "This PC" > "Local Disk (C:)".
- Right-click to create a new folder named "PHP".
- Install "PHPManagerForISS_V1.5.0" and "rewrite_amd64_en-US" from the zip file.
</p>
<br />

<p>
<img src="https://i.imgur.com/gAwb6WL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Extract PHP Files:

- Open the PHP installation zip and navigate to "php-7.3.8-nts-Win32-VC15-x86".
- Drag all contents into the "PHP" folder created earlier.
</p>
<br />

<p>
<img src="https://i.imgur.com/JWgGjIx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Install Additional Components:

- Install "VC_redist.x86" and "mysql-5.5.62-win32".
- Choose "Typical" setup for MySQL and configure with "Labpassword1".
</p>
<br />

<p>
<img src="https://i.imgur.com/4qSaDlu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Open IIS Manager:

- Search for "IIS" in the Windows search bar.
- Right-click "Internet Information Services (IIS) Manager" and select "Run as administrator".
</p>
<br />

<p>
<img src="https://i.imgur.com/SkxFaQF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/sMUrqGK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/nfGGfkS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Register PHP Version:

- Open "PHP Manager" within IIS Manager.
- Click "Register new PHP version" and navigate to the "php-cgi" file in the "PHP" folder.
- Restart IIS Manager after registration.
</p>
<br />

<p>
<img src="https://i.imgur.com/k6PY6nU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/nfGGfkS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Copy osTicket Files:

- Copy the "upload" folder from the "osTicket-v1.15.8" zip file.
- Paste the folder into "C:\inetpub\wwwroot" and rename it to "osTicket".
- Restart the server in IIS Manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/7Zt6XKf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Access osTicket Installer:

- In IIS Manager, expand "Sites" > "Default Web Site" > click "osTicket" > "Browse*:80(http)".
</p>
<br />

<p>
<img src="https://i.imgur.com/1XZVoKb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/Uq0vSFN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/d7PSm4x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. Enable PHP Extensions:

- Open PHP Manager and click "Enable or disable an extension".
- Enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll".
</p>
<br />

<p>
<img src="https://i.imgur.com/tiXFZ29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Rename Configuration File:

- Navigate to "C:\inetpub\wwwroot\osTicket\include" and rename "ost-sampleconfig.php" to "ost-config.php".
- Set appropriate permissions for "ost-config.php".
</p>
<br />

<p>
<img src="https://i.imgur.com/tg1qlj7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/ljpq1y9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/yre0UL1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/51wznYS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Rename Configuration File:

- Open the "Properties" window of the file "ost-config.php".

- Navigate to the "Security" tab within the "Properties" window.

- Click on the "Advanced" button at the bottom of the "Security" tab.

- In the "Advanced Security Settings for ost-config.php" window, locate and click on the "Disable inheritance" button. Confirm by selecting "Remove all inherited permissions from this object".

- After disabling inheritance, return to the "Advanced Security Settings" window.

- Click on the "Add" button to add a new permission entry.

- In the "Permission Entry" window, click on "Select a principal".

- Type "Everyone" in the text field and click "Check Names" to verify.

- Once verified, click "OK" to add "Everyone" as a new principal.

- In the "Permission Entry" window, ensure that all permissions are selected (typically Full Control, Modify, Read & Execute, Read, and Write).

- Click "OK" to confirm the selected permissions for "Everyone".

- Back in the "Advanced Security Settings" window, click "Apply" to apply the changes.

- Click "OK" to close the "Advanced Security Settings" window and save the changes.
</p>
<br />

<img src="https://i.imgur.com/AuTzaVz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Ky9rAlG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Complete osTicket Installation:

- Continue the osTicket installation in the browser, filling out the form with test information.
- Use "Password1" for all passwords.
</p>
<br />


<img src="https://i.imgur.com/YKzYFnw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/XhBbIiZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Install HeidiSQL:

- Install "HeidiSQL_12.3.0.6589_Setup" from the downloads folder and launch HeidiSQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/Cgb8dJp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/4BWHZib.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. Create Database in HeidiSQL:

- Create a new database named "osTicket" in HeidiSQL.
</p>
<br />

 <p>
<img src="https://i.imgur.com/g0BbVe9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. Finish osTicket Installation:

- Fill out remaining fields in the osTicket installation form with MySQL details.
- Click "Install Now" to complete the installation.
</p>
<br />

 <p>
<img src="https://i.imgur.com/t0Fc5dl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/XcX7wcI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. Finalize Configuration:

- Delete the "setup" folder in "C:\inetpub\wwwroot\osTicket".
- Adjust permissions for "ost-config.php" as before.
</p>
<br />

 <p>
<img src="https://i.imgur.com/aJthXvJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. Access osTicket:

- Log in to the osTicket Help Desk at http://localhost/osTicket/scp/login.php.
- Access the osTicket End User Page at http://localhost/osTicket/.

</p>
<br />

