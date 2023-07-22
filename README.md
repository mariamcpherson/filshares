<p align="center">
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/ae4e7768-a28b-461f-971a-59ebb98e03e4"/>
</p>

<h1>Network File Sharing and Persmissions</h1>
<p>
File Sharing allows us to distribute or provide access to digital files (such as documents, images, videos, audio, software, etc.) to multiple users or devices over a network or the internet. It enables users to exchange files with others, either collaboratively or for personal use, without having to physically transfer physical media like CDs or USB drives.
</p>
<p>
In this tutorial, we will explore the ins and outs of File Sharing and Permissions to access files in different folders. </p><br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
  
<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Windows Server 2022

<h2>Pre-requisites</h2>

- Direct Directory installed in Windows Server VM in Azure and set as Domain Controller
- Windows 10 VM in Azure joined to the Domain Controller

<h2>High-Level Steps</h2>

- Create File Share Folders in Domain Controller
- Step 2
- Step 3
- Step 4

<h2>Actions</h2>

<p>
In our Domain Controller Virtual Machine, we will create 4 folders in C:\
</p>

<p>
C:\read access
</p>
<p>
C:\write acess
</p>
<p>
C:\no access
</p>
<p>
C:\accounting
</p><br />

<p>
Now, we'll set the permissions for the first three folders (we'll go back to the "accounting" folder later), by right-clicking on the folder in question, Properties → Sharing → Share, then type "Domain Users", and set permission to Read.
</p>

<p>
<img src="(https://github.com/mariamcpherson/filshares/assets/139581822/3c9c1db5-a48b-4d10-8499-d7b6f2ba5c58)"/>
</p>

<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>
<p>



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br /># filshares
