<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create 2 Virtual Machines in Azure; one with Windows 10(Client-1) and the other with Windows Server 2022(DC-1)
- Install Active Directory Domain Services
- Create an Administrator Account
- Create non-administrative users

<h2>Deployment and Configuration Steps</h2>
Installed Active Directory Domain Services.
<img width="947" alt="Installing AD DS" src="https://github.com/brysonejones/configure-ad/assets/163891519/dfa1a93c-4d3c-4fd5-ad53-6813c1e106d2">
<img width="1582" alt="Installing AD DS 2" src="https://github.com/brysonejones/configure-ad/assets/163891519/9d6b486d-6921-440f-a875-1ccdbd450030">
</p>
<p>
Created an administrative user for Jane Doe(jane_admin) and then made it a member of Domain Admins.
<img width="690" alt="Admin Accnt creation" src="https://github.com/brysonejones/configure-ad/assets/163891519/824a24ec-8fec-4321-a9a2-f4d6d8a51793">
<img width="410" alt="Jane DA member" src="https://github.com/brysonejones/configure-ad/assets/163891519/e79734d0-c3a9-48a7-954d-9ce7c322c59e">
</p>
<p>
Joined Client-1 to mydomain.com on DC-1 by changing Client-1 DNS settings in Azure and point it to the Domain Controller on DC-1; also made Client-1 accessible by Remote Desktop so other non-admin users can login on the computer.
<img width="1710" alt="C1 domain addition" src="https://github.com/brysonejones/configure-ad/assets/163891519/bf34a554-c571-4114-a6bb-bf709f324763">
<img width="367" alt="C1 domain addition 2" src="https://github.com/brysonejones/configure-ad/assets/163891519/789850d2-4830-4e1e-b14d-f4d0b5185b1f">
<img width="859" alt="C1 domain addition 3" src="https://github.com/brysonejones/configure-ad/assets/163891519/a27b77ef-67ef-4558-8d0e-bcc88d12a572">
</p>
<p>
Generated some additional users with resources from class instructor. They were inserted into the Employees folder.
<img width="1297" alt="Normal users creation" src="https://github.com/brysonejones/configure-ad/assets/163891519/bda3f775-9544-4b75-a1de-1a595723b848">
<img width="957" alt="Normal users creation 2" src="https://github.com/brysonejones/configure-ad/assets/163891519/8cc024ae-45c7-42a5-bc47-e019eb237e54">
</p>
<p>
Logged in as one of the generated user accounts

<img width="1710" alt="User domain login 2" src="https://github.com/brysonejones/configure-ad/assets/163891519/3867dd61-52ac-4110-9772-0b4db6290197">
<img width="447" alt="User domain login" src="https://github.com/brysonejones/configure-ad/assets/163891519/dece4551-fb13-4b41-bbaf-039fa1e89238">
