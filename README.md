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
<br/>


<p>
Next we will connect to the VM using either Remote Desktop Connection on a PC or Microsoft Remote Desktop on a Mac. To connect grab the Public IP address from the VM and login using the Username and Password you made during the creation of the VM.
</p>

![image](https://user-images.githubusercontent.com/111653930/235473276-5c17744a-a14e-425f-8fd1-068f692072cc.png)

<br>


Once connected we will install / enable IIS in Windows with CGI. 


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

<br>

Now we will download the php file. Right click the file and hit Extract all. Now choose our newly created PHP folder in the root of C:


![image](https://user-images.githubusercontent.com/111653930/235523489-c78ab3b4-f600-475f-b16e-2ad8d6d88cdb.png)


After that we will download and install VC_redist.x86

![image](https://user-images.githubusercontent.com/111653930/235524296-78c66f23-48cf-4217-9b95-0774475409c2.png)

<br>

And last but not least we will download and install MySql Server. Accept the agreement and run a Typical install. 

![image](https://user-images.githubusercontent.com/111653930/235525127-54be54a4-fdf8-4f8f-b82e-deb56f91171b.png)
<br>



Following the configuration wizard select Standard Configuration and choose a root password:

![image](https://user-images.githubusercontent.com/111653930/235526906-2bcb4de5-5a44-4ffd-af9d-766f973ae884.png)


Next open IIS as an admin. Double click PHP Manager and select Register New PHP Version. Navigate to C: > PHP > and select the php-cgi file and select OK.

![image](https://user-images.githubusercontent.com/111653930/235528502-c1136453-67e1-4047-857a-ef20f0c61d64.png)


Next we download and install osTicket v 1.15.8. Extract and copy the "upload" folder to c:\inetpub\wwwroot. Once the file is copied rename it to "osTicket".

![image](https://user-images.githubusercontent.com/111653930/235529939-382680e1-3fa2-41c6-a23b-cbb848713a95.png)
![image](https://user-images.githubusercontent.com/111653930/235530190-ce6af00d-974d-4bb0-99c7-52d799f6bdc1.png)

<br>

Next reload Internet Information Services (as admin) and restart the server on the top right. Now go to sites - default - osTicket, and on the right click Browse *:80:

![image](https://user-images.githubusercontent.com/111653930/235531056-78596e09-165e-4d61-84bd-2fa567f370a9.png)

<br>

Note that some extensions are not enabled. Go back to Internet Information Services (as admin) and click sites > default > osTicket. Double click PHP Manager - Enable or disable an extension and enable the following extensions:
- php_imap.dll
- php_intl.dll
- php_opcache.dll

Now refresh the osTicket site in your browser and observer the change:

![image](https://user-images.githubusercontent.com/111653930/235532568-aacc28b5-a6c7-4bc3-a0f6-8d882df93e9a.png)





