<p align="center">
<img src="https://github.com/user-attachments/assets/fbbbc71e-033f-40fa-9529-a21f1334396b"  height="30%" width="30%"/>
</p>

<h1>File Sharing</h1>
In this lab, we will explore and experiment with how file share works. In this exercise, the goal is to enhance our knowledge of how file shares function between a server and a user.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 Pro (22H2)-Client 1
- Windows Server- DC-1(Domain Controller)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Virtual Network inside Azure Resource Group

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/user-attachments/assets/70f2f67d-7876-4788-9802-a6119c9efd16" height="50%" width="50%"/>
</p>

<p>
Create a Resource Group, as seen in the lab [Creating Virtual Machines within Azure](https://github.com/gustygreen/Azure). Create and add a Virtual Network. Create and add the Domain Controller. Create and add the Client.
<br />
<p>

  
<h2>Lab Steps</h2>
<h3>Create folders on DC to setup access</h3>
<p>
<img src="https://github.com/user-attachments/assets/31333106-6453-4d80-a845-f85664ebfa33" heigth="50%" width="50%"/>
</p>
<p>
Create 4 folders on DC-1 C:\Windows directory. Label them "read-access", "write-access", "no-access", and "finance".

<p>
<img src="https://github.com/user-attachments/assets/5895fd21-0b47-4832-841c-510aba241a68" heigth="50%" width="50%"/>
</p>
<p>
Set the proper sharing access for each folder. Right click the folder(1), select Properties, select Sharing(2), click Share(3). Type "Domain Users" in the Name field(4) and select Add(5).   
</p>

<p>
<img src="https://github.com/user-attachments/assets/afbc456d-dd36-4550-9044-c0490de78afe" heigth="50%" width="50%"/>
</p>
<p>
Set the Domain Users permission level to "Read". Select "Share".  
</p>

<p>
<img src="https://github.com/user-attachments/assets/9ea56cdd-976b-4dbb-a6c8-ae4166bef995" heigth="50%" width="50%"/>
</p>
<p>
Set the "write-access" folder to have Domain Users permission level set to "Read/Write". Select "Share".  
</p>

<p>
<img src="https://github.com/user-attachments/assets/6dd0d10b-80e3-4d15-8517-abda988a1c15" heigth="50%" width="50%"/>
</p>
<p>
Set the "no-access" folder to have Domain Admins permission level set to "Read/Write". Select "Share".  
</p>

<p>
<img src="https://github.com/user-attachments/assets/eafcaa90-e070-4f6b-8614-4fb54f0712fc" heigth="50%" width="50%"/>
</p>
<p>
On Client-1 login as a normal user(Domain User) Access dc-1 through File explorer. You will see the shared folders available. 
</p>

<p>
<img src="https://github.com/user-attachments/assets/22c63f26-9899-4fe9-911e-fd65e8bb874d" heigth="50%" width="50%"/>
</p>
<p>
On Client-1 login as a normal user, they have read only access for the read-access folder so when trying to create a file they will not be able to do so. 
</p

<p>
<img src="https://github.com/user-attachments/assets/604c8994-49e2-4288-b5b4-ac3edbe3ae4f" heigth="50%" width="50%"/>
</p>
<p>
On Client-1 login as a normal user, they have read/write access for the write-access folder so when trying to create a file, they are able to do so. 
</p

<p>
<img src="https://github.com/user-attachments/assets/ed13db02-89fb-4df2-967f-9b1b6f4412a2" heigth="50%" width="50%"/>
</p>
<p>
On Client-1 login as a normal user, they are not part of the Domain Admins group so when access the no-access folder, they will not be able to do so.
</p>

This concludes the lab on file sharing.
