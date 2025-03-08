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

- Create a Virtual Network (VNet)
- Deploy an Azure Virtual Machine for AD
- Configure VM for Active Directory

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/0w1JsUP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Azure, create a Virtual Network (VNet) for the AD servers.
Set up subnets (e.g., one for AD DCs, one for application servers).
Configure private IP addresses for stable connectivity.
</p>
<br />

<p>
<img src="https://i.imgur.com/2isNBgd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new Windows Server VM (Windows Server 2019/2022).
Assign a static private IP to avoid IP changes affecting the domain controller.
Enable RDP access (limit to trusted IPs for security).
</p>
<br />

<p>
<img src="https://i.imgur.com/4pOq3nA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set the VM’s DNS settings to point to itself (127.0.0.1) or an existing AD DNS.
Install the Active Directory Domain Services (AD DS) role via Server Manager or PowerShell.
</p>
<br />
