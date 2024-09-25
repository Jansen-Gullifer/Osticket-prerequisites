# Osticket-prerequisites
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Tutorial </h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- OS Ticket installation files
- Enable IIS with CGI
- Install PHP manager 
- Intall Rewrite module (rewrite_amd64_en-US.msi)
- Create the directory C:\PHP
- Install VC_redist.x86.exe.
- Install MySQL 5.5.62

<h2>Installation Steps</h2>

<p>
//Step 1: Create a Resource Group
Log in to Azure Portal: Go to the Azure portal (portal.azure.com) and sign in with your account.
Create a Resource Group:
Click on “Resource groups” in the left-hand menu.
Click the “+ Create” button.
Fill in the Resource group name and select your Region.
Click “Review + Create,” then click “Create.”
  
//Step 2: Create a Virtual Machine
Navigate to Virtual Machines:

Click on “Virtual machines” in the left-hand menu.
Click the “+ Create” button and select “Virtual machine.”
Configure Basic Settings:

Select the Resource Group you created.
Fill in the Virtual machine name.
Choose your Region.
Select the Image (e.g., Windows Server).
Choose the Size (e.g., Standard B1s).
Create or select an Admin username and Password.
Configure Networking:

Under the “Networking” tab, select the default settings or adjust as needed.
Ensure that Public inbound ports are set to allow RDP (Port 3389).
Review and Create:

Click “Review + Create,” review your settings, and click “Create.” Wait for the deployment to complete.

//Step 3: Create a Remote Desktop Connection
Get the Public IP Address:

Once the VM is deployed, go to the Virtual Machines section, select your VM, and note the Public IP address.
Establish Remote Desktop Connection:

Open the Remote Desktop Connection application on your local machine.
Enter the Public IP address of the VM.
Click “Connect.”
Enter the Admin username and Password you set during VM creation.
Click “OK” to connect.

![image](https://github.com/user-attachments/assets/37fdb2ed-d943-4781-bd20-f1c54c8c08c4)


<p>
//Step 1: Download and Prepare osTicket Files
Download osTicket:
Inside the VM (osticket-vm), download the osTicket-Installation-Files.zip.
Unzip it onto your desktop. This should create a folder named osTicket-Installation-Files.

//Step 2: Install and Configure IIS
Install IIS:
Open the Control Panel and navigate to Programs > Turn Windows features on or off.
Expand Internet Information Services and then World Wide Web Services.
Under Application Development Features, check the box for CGI.
Click OK to install IIS with CGI support.

//Step 3: Install PHP and Required Components
Install PHP Manager for IIS:

From the osTicket-Installation-Files folder, run PHPManagerForIIS_V1.5.0.msi and follow the prompts to install it.
Install URL Rewrite Module:

From the same folder, run rewrite_amd64_en-US.msi to install the Rewrite Module.
Set Up PHP Directory:

Create a new directory: C:\PHP.
Install PHP:

From the osTicket-Installation-Files folder, unzip php-7.3.8-nts-Win32-VC15-x86.zip into the C:\PHP folder.
Install Visual C++ Redistributable:

Run VC_redist.x86.exe from the osTicket-Installation-Files folder to install the necessary libraries.

//Step 4: Install MySQL
Install MySQL:

Run mysql-5.5.62-win32.msi from the osTicket-Installation-Files folder.
Choose Typical Setup during installation.
Configure MySQL:

After installation, launch the MySQL Configuration Wizard.
Select Standard Configuration.
Set the Username to root and Password to root.
</p>

![image](https://github.com/user-attachments/assets/2898016a-1674-4b89-8b1b-5bdd9dbfce28)


</p>
//Step 1: Prepare IIS and PHP
Open IIS as Admin and register PHP:
Right-click the IIS icon and select Run as administrator.
In PHP Manager, register PHP using C:\PHP\php-cgi.exe.
Enable CGI in Control Panel > Programs > Turn Windows features on or off > Internet Information Services > World Wide Web Services > Application Development Features.
Reload IIS by stopping and starting the server.

//Step 2: Install osTicket
Download and Set Up osTicket:
Unzip osTicket-v1.15.8.zip from the osTicket-Installation-Files folder.
Copy the upload folder to C:\inetpub\wwwroot and rename it to osTicket.
Access osTicket via http://localhost/osTicket, then enable necessary PHP extensions (php_imap.dll, php_intl.dll, php_opcache.dll) through PHP Manager.

//Step 3: Configure Database
Prepare Configuration:
Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to ost-config.php.
Set permissions for ost-config.php to allow Full Control for Everyone.
Install HeidiSQL from the installation files and create a new session (Username: root, Password: root).
Create a database named osTicket.

//Step 4: Complete Installation
Finish osTicket Setup:
In the osTicket setup, input the database details:
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click Install Now! Once installed, access:
Helpdesk login: http://localhost/osTicket/scp/login.php
End Users URL: http://localhost/osTicket/
Clean up by deleting the setup folder and setting ost-config.php to Read Only.

<p>

![image](https://github.com/user-attachments/assets/4340a42c-f325-43cc-9ef3-569b03222548)


</p>
<br />
