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

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
