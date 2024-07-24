<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute part 1](https://www.youtube.com/watch?v=XopnGvXPs10)
- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute part 2](https://www.youtube.com/watch?v=58qJ8B_YV9s)


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Create an Admin and Normal User Account in AD
- Join Client-1 to your domain (mydomain.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>

![Screen Shot 2024-07-23 at 5 51 53 PM](https://github.com/user-attachments/assets/9b242f18-0b24-448d-b3bf-01361f54d5c9)
</p>
<p>
In this step, all of the needed resources needed to run this lab were created (VM using Windows Server 2022 OS named Domain Controller 1 [DC-1] and VM using Windows 10 OS named Client-1).
</p>
<br />



<p>

![Screen Shot 2024-07-23 at 6 18 04 PM](https://github.com/user-attachments/assets/7d812143-86fe-4fd5-8529-e181aadcd0ca)
![Screen Shot 2024-07-23 at 6 21 26 PM](https://github.com/user-attachments/assets/2d3cc0e8-03b2-4f73-bd8b-b9d1e8ed94e2)
![Screen Shot 2024-07-23 at 6 20 10 PM](https://github.com/user-attachments/assets/f3cb0bad-f90b-44b7-a801-4da389d031e4) 
![Screen Shot 2024-07-23 at 6 05 42 PM](https://github.com/user-attachments/assets/a96f0f64-2864-41d0-a2e1-341202b591a6)
</p>
<p>
During this step, in order to test the connectivity between VM Client-1 and VM DC-1, we 1st login to Client-1 with Remote Desktop and attempt a perpetual ping to DC-1’s private IP address, with no initial success.  Then we login into DC-1, enable ICMPv4 in on the local windows Firewall, then check back into Client-1 to see the perpetual ping begin to succeed. 
</p>
<br />



<p>
  
![Screen Shot 2024-07-23 at 6 34 40 PM](https://github.com/user-attachments/assets/39566b12-628b-443a-8d3c-10615a088acb)
![Screen Shot 2024-07-23 at 6 32 40 PM](https://github.com/user-attachments/assets/c44e1a61-9a07-4520-b6c3-739921e41a5c)
![Screen Shot 2024-07-23 at 6 34 06 PM](https://github.com/user-attachments/assets/8954d1c8-a252-4217-baac-19420fcd383d)
<p>
In this step, we installed Active Directory into DC-1.
</p>
<br />



<p>

![Screen Shot 2024-07-23 at 6 50 23 PM](https://github.com/user-attachments/assets/15990d3a-66e2-4ba1-a937-f0b5be2add08)
![Screen Shot 2024-07-23 at 6 51 07 PM](https://github.com/user-attachments/assets/5eefd7ca-a48b-4c31-8b41-69e84ac7235c)
![Screen Shot 2024-07-23 at 6 51 51 PM](https://github.com/user-attachments/assets/b57674fe-8396-4d12-9bce-284174eb08d1)
</p>
<p>
In this step, we created an admin/normal user account in Active Directory.  This account is an adminstative employee account for an employee named Jane Doe, and her username is jane_admin.  Jane_admin is the only username/admin account used for DC-1 from this point moving forward.
</p>
<br />



<p>
  
![Screen Shot 2024-07-23 at 8 03 31 PM](https://github.com/user-attachments/assets/5ba6217e-2871-4eaf-9695-a669d5679267)
</p>
<p>
In this step, we joined Client-1 to the domain (mydomain.com).  Basically, this means that Client-1 shows up in Active Directory Users and Computers inside of DC-1.
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
<br />
