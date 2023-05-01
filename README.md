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

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>Welcome to my first tutorial! To get things started we will create a new Virtual Machine using the Microsoft Azure Platform. Begin by creating a new resource group called "RG-osTicket". Once your resource group is made create a new Virtual Machine and name it "vm-osticket". Make sure this Virtual Machine is set to Windows 10 and has 2-4 vcpu's.</p>

![image](https://user-images.githubusercontent.com/111653930/235471893-c5bb8b4b-3e13-4ec1-bef5-6daac2fbd079.png)

<p>
Next we will connect to the VM using either Remote Desktop Connection on a PC or Microsoft Remote Desktop on a Mac. To connect grab the Public IP address from the VM and login using the Username and Password you made during the creation of the VM.
</p>

![image](https://user-images.githubusercontent.com/111653930/235473276-5c17744a-a14e-425f-8fd1-068f692072cc.png)

<br />

<p>
Once connected we will install / enable IIS in Windows with CGI. 
</p>

![image](https://user-images.githubusercontent.com/111653930/235476668-87ed5a24-95e2-4900-b2b7-cfdb6e727a1c.png)

<p> Next we will begin downloading and installing all the necessary files to run osTicket. All files are available here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

To start download and install PHP Manager for IIS.</p>

![image](https://user-images.githubusercontent.com/111653930/235494410-b5fb0fcc-291e-4bb7-9953-02812dc023c7.png)

<br>
<p> Following the PHP Manager we will install the Rewrite Module. </p>


![image](https://user-images.githubusercontent.com/111653930/235495727-eff79be9-b6c8-4fcf-9b20-d89cb62da4db.png)

<br>


Next we will create a directory for PHP on the local harddrive. Navigate to the root of the C: drive and right click - New - Folder, and name it PHP.

![image](https://user-images.githubusercontent.com/111653930/235520886-58cbffdf-4313-4392-aebd-16d32efbe2f8.png)


