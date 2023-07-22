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

- Create File Share Folders in Domain Controller and assign permissions
- Check acees to shared folders from Client VM (Windows 10)

<h2>Actions</h2>

<p>
In our Domain Controller Virtual Machine, we will create 3 folders in C:\
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
<br />

<p>
Now, we'll set the permissions for the  three folders by right-clicking on the folder in question, Properties → Sharing → Share, then type "Domain Users", and set permission to Read. Files in this folder can be accessed by all domain users, but they cannot make changes to those files.
</p>

<p>
<img src="(https://github.com/mariamcpherson/filshares/assets/139581822/3c9c1db5-a48b-4d10-8499-d7b6f2ba5c58)"/>
</p>

<p>
Now, do the same for the "write access" folder, but set the Attribute to "Read/Write." 
</p>

<p>
And for the "no access" folder: Properties → Sharing → Share, then type "Domain Admins", and set permission to Read/Write. This means that only Domain Admins can access the files inside that folder and make changes to them. 
</p>

<p>
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/1647dfbc-e7bb-459f-a609-b47b240c94a0"/>
</p>


<p>
- Step 2:
</p>
<p>
Let's check those permissions from our Client machine. I will log in into the Windows 10 machine as the random user I selected in the previous tutorial>
</p>

<p>
mydomain.com\bowa.mudo
</p>
<p>
Password1
</p>

<p>
This user is not an admin, he is part of the Domain Users group, so we should expect for them to not be able to create a new file in "read access" folder, but only in the "write access" folder, and no access to the files inside "no access."
</p>


<p>
In order to access the folders which are hosted in our Domain Controller Machine, we can go to the File Explorer and type \\(name of the VM). In my case, I named my Server VM DC-1 when I created it in Azure so I'll type \\dc-1
</p>

<p>
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/2e055445-cae3-4d66-b575-a6776711251c"/>
</p>

<p>
When bowa.mudo tries to access the "no access" folder, he is not able to, because he is not part of Domain Users, and only they can access this folder.
</p>

<p>
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/b9b3c0b2-790c-49d3-a585-a8a78afa36af"/>
</p>

<p>
When bowa.mudo tries to create a plain text file in the "read access" folder, they're not able to because Domain Users can only view files in this folder.
</p>

<p>
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/f4ca79d4-286f-41cb-920b-bd3f67f6a605"/>
</p>


<p>
Now, bowa.mudo can create a plain text file inside the "write access" folder because this folder has permissions set in such a way that members of Domain Users can create and view files.
</p>

<p>
<img src="https://github.com/mariamcpherson/filshares/assets/139581822/677199b1-a261-4cff-90cf-cf73e6438937"/>
</p>
