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

<p>
<img width="3199" height="1799" alt="image" src="https://github.com/user-attachments/assets/277f8b69-b6ef-4bb5-86bd-ab38d1e50e2d" />
</p>
<p>
After configuring MySQL, you'll want to run IIS as administrator.
</p>
<br />

<p>
<img width="2492" height="1298" alt="image" src="https://github.com/user-attachments/assets/16d59318-a573-49d2-9b4c-22689054bf82" />
</p>
<p>
Inside IIS, You'll want to double click on the PHP Manager.
</p>
<br />

<p>
<img width="2492" height="1303" alt="image" src="https://github.com/user-attachments/assets/18eff35d-7f9e-48dd-9177-b0bed8d4cdd2" />
</p>
<p>
<img width="2489" height="1297" alt="image" src="https://github.com/user-attachments/assets/afdf1ba5-c69a-4656-b27a-08211a6265f8" />  
</p>
<p>
You'll then want to register the PHP from your C:\PHP Directory you created earlier.
</p>
<br />

<p>
<img width="2486" height="1302" alt="image" src="https://github.com/user-attachments/assets/cb91b9a0-4c2c-43c8-8698-c2bee5ddac9a" />
</p>
<p>
<img width="2485" height="1295" alt="image" src="https://github.com/user-attachments/assets/ccd208c4-31ad-4ad5-9923-57631cb1df83" />
</p>
<p>
With nothing selected in IIS, Navigate to the far right Actions panel to stop and restart the server to initiate the changes to the PHP Configuration.
</p>
<br />

<p>
<img width="1974" height="1106" alt="image" src="https://github.com/user-attachments/assets/1a36e77a-0ab0-4da8-a8fe-79a3d315664d" />
</p>
<p>
Inside the "osTicket-Installation-Files" folder on the VM desktop is a compressed Zip file named "osTicket-v1.15.8". Unzip it / Extract All.
</p>
<br />

<p>
<img width="1975" height="1102" alt="image" src="https://github.com/user-attachments/assets/96ffc168-40f2-4857-a934-ba287f62b9cb" />
</p>
<p>
Inisde that osTicket-v1.15.8 folder that was just extracted there will be two more folders titled "upload" and "scripts". You'll want to copy that upload folder and paste it to the following directory.
C:\inetpub\wwwroot  
</p>
<br />

<p>
<img width="1966" height="1103" alt="image" src="https://github.com/user-attachments/assets/bd14a8be-0ae7-4501-89e1-253b5b98b7d8" />
</p>
<p>
After pasting the upload folder into the C:\inetpub\wwwroot directory, you'll want to rename the upload folder you just pasted to "osTicket".
</p>
<br />

<p>
<img width="2486" height="1302" alt="image" src="https://github.com/user-attachments/assets/cb91b9a0-4c2c-43c8-8698-c2bee5ddac9a" />
</p>
<p>
<img width="2485" height="1295" alt="image" src="https://github.com/user-attachments/assets/ccd208c4-31ad-4ad5-9923-57631cb1df83" />
</p>
<p>
With nothing selected in IIS, Navigate to the far right panel to stop and restart the server to initiate the changes to the wwwroot configuration.
</p>
<br />

<p>
<img width="2493" height="1300" alt="image" src="https://github.com/user-attachments/assets/9c0569b3-5c7e-4937-9914-6a147837f042" />
</p>
<p>
On the left side connetions panel in IIS, click through the drop downs to navigate to your osTicket folder you just renamed. With the folder selected click on the "browse*:80(http)" located on the far right panel inside of IIS.
</p>
<br />

<p>
<img width="3199" height="1799" alt="image" src="https://github.com/user-attachments/assets/4a50295e-5f04-4706-8459-8c1a1240a5b3" />
</p>
<p>
With everything done correctly, clicking on browse*:80(http) will redirect you to the osTicket install page. BUT as you can tell, there are some X marks on some extensions that need to be enabled.
</p>

<p>
<img width="1592" height="1708" alt="image" src="https://github.com/user-attachments/assets/206c6a78-3efc-498a-937b-2c4728ee1181" />
</p>
<p>
<img width="1599" height="1713" alt="image" src="https://github.com/user-attachments/assets/ca012786-7f75-4261-bf7b-0436bab3a8ac" />
</p>
<p>
In IIS, with the osTicket folder still selected through the drop downs from the connections panel, Open PHP Manager. Once inside PHP Manager you'll want to navigate to "Enable or disable extensions".
</p>
<br />

<p>
<img width="1599" height="1713" alt="image" src="https://github.com/user-attachments/assets/1f2f98d5-c59d-4664-b560-7fa67172229f" />
</p>
<p>
<img width="1595" height="1712" alt="image" src="https://github.com/user-attachments/assets/dc3a98b9-6f28-4075-a1ed-93917e4e151f" />
</p>
<p>
The 3 extensions we want to enable are called "php_imap.dll" "php_intl.dll" "php_opcache.dll". They're enabled by clicking on the one you want and clicking "enable" on the far right panel in the top right corner of IIS.
</p>
<br />

<p>
<img width="1592" height="1713" alt="image" src="https://github.com/user-attachments/assets/02419d40-8ae3-4abf-b773-1829cbbf5199" />
</p>
<p>
After making those changes to the extensions, we can refresh the page for osTicket and see that all of our requirements have been met. The two X's at the bottom are only neeeded for faster performance.
</p>
<br />

<p>
<img width="1961" height="1104" alt="image" src="https://github.com/user-attachments/assets/9bafd6e9-f411-419c-9daf-fa7fe884b827" />
</p>
<p>
<img width="1964" height="1103" alt="image" src="https://github.com/user-attachments/assets/dbffcc07-fbe4-4dbf-a1c8-f92024832eb3" />
</p>
<p>
In your files navigate to the directory "C:\inetpub\wwwroot\osTicket\include\". Locate the file "ost-sampleconfig.php" and rename it to "ost-config.php".
</p>
<br />

<p>
<img width="1967" height="1100" alt="image" src="https://github.com/user-attachments/assets/a5c56b7a-a512-4d0c-b412-cec148474a36" />
</p>
<p>
<img width="743" height="932" alt="image" src="https://github.com/user-attachments/assets/16789273-2d05-4471-96f9-3ec05642259a" />
</p>
<p>
Right click the file you just renamed, and click on properties. Then navigate to the Security tab, and click advanced to edit the permissions for this file. Our goal is to add a new permission to allow osTicket to make any changes to this file. We will also be removing any other permissions attached to this file before doing so.
</p>
<br />

<p>
<img width="1407" height="952" alt="image" src="https://github.com/user-attachments/assets/95e1bbd0-12da-45a0-b78f-739964636050" />
</p>
<p>
When inside the advanced security settings, click on "disable inheritance" this will cause a pop up. You'll then want to select "Remove all inherited permissions from this object.".
</p>
<br />

<p>
<img width="1398" height="943" alt="image" src="https://github.com/user-attachments/assets/7df4dda9-f7c7-4c5b-b218-2dff177d0008" />
</p>
<p>
Click Add.
</p>
<p>
<img width="1678" height="1081" alt="image" src="https://github.com/user-attachments/assets/d3ffd296-b1de-404b-8e74-993d7af0de99" />
</p>
<p>
Navigate to "select a principal" at the top of the window.
</p>
<p>
<img width="1679" height="1085" alt="image" src="https://github.com/user-attachments/assets/6a8d9e0d-d1a1-4f97-8322-800c9158b159" />
</p>
<p>
Type "everyone" in the box and click ok.
</p>
<p>
<img width="1675" height="1086" alt="image" src="https://github.com/user-attachments/assets/eeb91538-5d66-4243-ae42-0ec7dc01c6aa" />
</p>
<p>
Check the box that says "full control" then click Ok
</p>
<br />

<p>
<img width="1404" height="947" alt="image" src="https://github.com/user-attachments/assets/89f6fc08-f757-44fb-aa18-b8e50ca8160c" />
</p>
<p>
Click apply to apply the changes, then click Ok to exit the advanced security settings.
</p>

<p>
<img width="1596" height="1715" alt="image" src="https://github.com/user-attachments/assets/fed79365-1336-4562-b735-44d6fcfcddc6" />
</p>
<p>
Go back to your open osTicket website and continue with the install. 
</p>
<br />

<p>
<img width="1596" height="1713" alt="image" src="https://github.com/user-attachments/assets/358eadfc-e9f0-41d5-8164-6b44a4798b56" />
</p>
<p>
You'll want to fill in the information on screen. For your admin user info be sure to write it down for safe keeping.
</p>
<br />

<p>
<img width="3199" height="1799" alt="image" src="https://github.com/user-attachments/assets/5e0aa8fd-2a85-4162-85ec-e49b1efb8741" />
</p>
<p>
Inside the "osTicket-Installation-Files" folder on the VM desktop is a program called "HeidiSQL_12.3.0.6589_Setup". We will need to run this application to set up our database and configure it for osTicket.
</p>
<br />

<p>
<img width="995" height="811" alt="image" src="https://github.com/user-attachments/assets/3a078a35-7393-43f9-9dfc-f2b84eab0907" />
Accept and click next.
</p>
<p>
<img width="994" height="805" alt="image" src="https://github.com/user-attachments/assets/d0fbfbf4-74ed-4d78-b889-a1d6bbb8fe52" />
  Continue to click next until HeidiSQL is installed and ready to launch.
</p>
<br />

<p>
<img width="1200" height="841" alt="image" src="https://github.com/user-attachments/assets/2f90b192-18f8-4c61-abf4-9f69b55c9f1a" />
</p>
<p>
In HeidiSQL you'll want to click "New" to start a new session. Fill in the username and password and keep it stored in a safe location, then click open to prepare for creating the osTicket database.
</p>
<br />

<p>
<img width="1708" height="895" alt="image" src="https://github.com/user-attachments/assets/4f595649-2579-4f41-8a9d-70e7af979988" />
</p>
<p>
In HeidiSQL, right click on the dolphin icon labeled "unnamed", hover over "create new", and click on database.
</p>
<br />

<p>
<img width="1710" height="899" alt="image" src="https://github.com/user-attachments/assets/caec672c-cd3a-49de-896f-632ae6e8e607" />
</p>
<p>
You'll want to title the database "osTicket" then click ok when finished.
</p>
<br />

<p>
<img width="3199" height="1797" alt="image" src="https://github.com/user-attachments/assets/fd3ea3c1-44cd-4cd1-815e-f893f1a8b8dd" />
</p>
<p>
After the database has been created, you will want to go back to the osTicket webpage where we started filling in the information for the install. At the bottom of the page you will need to type in the name of the database, as well as the username and password you set for MySQL. Click install when all information on the page has been filled in.
</p>
<br />

<p>
<img width="3199" height="1799" alt="image" src="https://github.com/user-attachments/assets/004fad9e-84dd-4556-963b-c26d8d490be6" />
</p>
<p>
<img width="3199" height="1799" alt="image" src="https://github.com/user-attachments/assets/27ab4791-2cab-4b25-9e4a-79da8cc687a1" />
</p>
<p>
osTicket should be successfully installed, and you should be able to log in with the admin credentials you created on the install page.
</p>
<br />

<p>
<img width="1123" height="630" alt="image" src="https://github.com/user-attachments/assets/40e678e6-ef2d-4085-8870-0a1eb0891a69" />
</p>
<p>
Open your file explorer, and navigate to the directory "C:\inetpub\wwwroot\osTicket" and delete the folder titled "setup". This is some post install clean up that osTicket will remind you to do if not done.
</p>
<br />

<p>
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d018e731-5634-4257-a0ea-adab0249384f" />
</p>
<p>
You'll also need to navigate to the directory "C:\inetpub\wwwroot\osTicket\include" and locate the file ost-config.php. Right click on it, click on properties, then click on the security tab. Then you'll click edit to change the permissions to read only. Every box should be unchecked besides the one labeled read. Click apply to save the changes then you're able to close out of file explorer.
</p>
<br />
