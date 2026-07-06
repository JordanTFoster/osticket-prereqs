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

- Windows 11 Pro</b> (25H2)

<h2>List of Prerequisites</h2>

- Create an Azure Virtual Machine. (Windows 11 Pro)
- Log into the VM with Remote Desktop
- Install / Enable IIS with CGI in Windows (Internet Information Services)
- Download the [osTicket-Installation-Files.zip](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download) to the desktop of the VM.

<h2>Installation Steps</h2>

<p>
<img width="1920" height="1080" alt="68 220 176 91 - Remote Desktop Connection 7_5_2026 7_19_54 PM" src="https://github.com/user-attachments/assets/0c6ab31e-9b9e-4a2c-b18d-ea183cb2820c" />
</p>
<p>
Inside the "osTicket-Installation-Files" folder on the VM desktop, is a file called "PHPManagerForIIS_V1.5.0". This installs the PHP Manager for IIS. After that is complete you'll want to locate the file "rewrite_amd64_en-US" and install it, this is the Rewrite Module for IIS. 
</p>
<br />

<p>
<img width="1920" height="1080" alt="68 220 176 91 - Remote Desktop Connection 7_5_2026 7_21_40 PM" src="https://github.com/user-attachments/assets/e23db6c6-58de-48e3-bbdb-cc74be859c3e" />
</p>
<p> 
After installing both the PHP Manager & Rewrite Module, navigate to the C: Drive and create the directory "C:\PHP". 

(This PC - C: Drive - Right click - Create new folder - Title it PHP)
</p>
<br />

<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2d9014c1-172d-47ec-b45f-772266e2e3ea" />
</p>
<p>
Unzip (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
</p>
<br />

<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d1caa697-fce0-4d8d-b21d-fb3197e24726" />
</p>
<p> 
Inside the "osTicket-Installation-Files" folder on the VM desktop are 2 files. VC_redist.x86.exe & mysql-5.5.62-win32. For the Install of MySQL you will want to do the typical setup.
</p>
<br />
  
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/273a441b-a955-4d77-aeba-e14ffd6046ba" />
</p>
<p>
After Installing, launch the Configuration Wizard to start configuring MySQL.
</p>
<br />

<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fdf035eb-dce8-4bac-b63a-ab7e1be36106" />
</p> 
<p>
You'll want to select the Standard Configuration.   
</p>
<br />

<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2865ad00-8775-4692-946e-621642dd65b3" />
</p>
<p>
Set the username to "root" and the password to "root". (NOTE: NEVER DO THIS FOR ACTUAL SYSTEMS) 
</p>
<br />
