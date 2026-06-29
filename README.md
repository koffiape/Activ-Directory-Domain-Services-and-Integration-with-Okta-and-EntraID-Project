
<h1>Active Directory Domain Services and Integration with Okta and Entra ID - Home Project</h1>

<h2>Description</h2>
In this project, I designed and implemented a fully functional Identity and Access Management (IAM) home lab using virtual machines to simulate a real-world enterprise environment. The lab included the configuration of Active Directory Domain Services (AD DS), the deployment of NAT and DHCP servers, the creation of over 1,000 users assigned to various groups, and the application of group policies to manage permissions and security settings. Additionally, I integrated the AD domain with Okta and Microsoft Entra ID (Azure AD), enabling seamless Single Sign-On (SSO) and hybrid identity management. Cloud synchronization was performed using Microsoft Entra ID to ensure centralized identity management across on-premises and cloud-based environments.
<br />
<p align="center">
<img src="https://imgur.com/jii6PUT.png" height="85%" width="85%" alt="Active Directory Homelab Setup"/>
</p

<h2>Languages and Environments Used (PaaS Components) </h2>


- <b>Azure</b>
- <b>Active Directory Domain Services</b>
- <b>PowerShell</b>
- <b>Windows 10 ISO</b>
- <b>Windows Server 2012 ISO</b>
- <b>Windows Server 2019 ISO</b>
- <b>VirtualBox</b>
- <b>Okta</b>
- <b>Entra ID</b>
- <b>Cloud Sync<b>

<h2>Project walk-through:</h2>

<p align="center">
Deploy Virtual Machine and configure IP settings: <br/>
<img src="https://imgur.com/jLoz7Tz.png" height="80%" width="80%" alt="Deploy Virtual Machine and configure IP"/>

 <p align="center">
Install Active Directory Domain Services: <br/>
<img src="https://imgur.com/rgT3u0S.png" height="80%" width="80%" alt="Active Directory Domain Service Installation"/>
<img src="https://imgur.com/vpDjEyM.png" height="80%" width="80%" alt="Complete Installation"/>

<p align="center">
Configuration of Active Directory Domain Services: <br/>
<img src="https://imgur.com/Wmn26Kp.png" height="80%" width="80%" alt="Deployment Configuration"/>
<img src="https://imgur.com/4e0L2a1.png" height="80%" width="80%" alt="Domain Controller Configuration"/>
<img src="https://imgur.com/MYwgCSL.png" height="80%" width="80%" alt="Passed Validation of Configuration"/>
<img src="https://imgur.com/zutjmEt.png" height="80%" width="80%" alt="Complete"/>

<br />
<br />
<p align="center">
Configure Remote Access Server and NAT: <br/>
<img src="https://imgur.com/O8XQv3T.png" height="80%" width="80%" alt="Install Remote access"/>
<img src="https://imgur.com/UxuFWnF.png" height="80%" width="80%" alt="Install Remote Access"/>
<img src="https://imgur.com/zsWb4oZ.png" height="80%" width="80%" alt="Remote Access Installation Complete "/>
<img src="https://imgur.com/0H6bKae.png" height="80%" width="80%" alt="Configure and Enable Remote Access"/>
<img src="https://imgur.com/DY8RC4v.png" height="80%" width="80%" alt="Configure and Enable Remote Access and NAT"/>
<img src="https://imgur.com/YAZLose.png" height="80%" width="80%" alt="Configure NAT"/>
<img src="https://imgur.com/PuXlbz3.png" height="80%" width="80%" alt="Configuration Complete"/>
<br />
<br />

<p align="center">
Configure DCHP Server: <br/>
<img src="https://imgur.com/zLim0Zs.png" height="80%" width="80%" alt="Start Installation"/>
<img src="https://imgur.com/V5o7lzf.png" height="80%" width="80%" alt="Finish Installation"/>
<img src="https://imgur.com/4rzYZ87.png" height="80%" width="80%" alt="New Scope DCHP configuration "/>
<img src="https://imgur.com/b9dzIHT.png" height="80%" width="80%" alt="Network Configuration within new DCHP scope"/>
<img src="https://imgur.com/fm09l90.png" height="80%" width="80%" alt="Lease Date Configuration"/>
<img src="https://imgur.com/mtxgRSn.png" height="80%" width="80%" alt="Router/Default Gateway Configuration"/>
<img src="https://imgur.com/J3PWvjL.png" height="80%" width="80%" alt="Domain Name and DNS Configuration"/>
<img src="https://imgur.com/VdHgbvs.png" height="80%" width="80%" alt="Configuration Complete"/>

<p align="center">
Create AD Users using PowerShell: <br/>
Create 1000 AD Users using Create_AD_Users.ps PowerShell script
<img src="https://imgur.com/jaVvza1.png" height="80%" width="80%" alt="Create 1000 new users"/>
<img src="https://imgur.com/Qgc3oFO.png" height="80%" width="80%" alt="AD Users Creation Complete"/>
<br />
<br />

<p align="center">
Create and Configure Windows 10 and Join to AD DS: <br/>
<img src="https://imgur.com/jkOPeN6.png" height="80%" width="80%" alt="VM Network Adapter Configuration"/>
<img src="https://imgur.com/Icjxejo.png" height="80%" width="80%" alt="Windows IP Configuration"/>
<img src="https://imgur.com/CwDt4O4.png" height="80%" width="80%" alt="Join Client 1 machine to mydomain.com"/>
<img src="https://imgur.com/9inlZWw.png" height="80%" width="80%" alt="Verification Client 1 successful joined to AD DS"/>

<br />
<br />
<h2>Active Directory Integration with Okta:</h2>
<p align="center">

<img src="https://imgur.com/IncxQmX.png" height="80%" width="80%" alt="Active Directory Integration with Okta"/>  

 <p align="center">
- <b>Download OktaADAgent and Install on AD DS Server </b>

<img src="https://imgur.com/nnUSSW4.png" height="80%" width="80%" alt="After Installing OktaADAgent on AD DS Server"/> 

<img src="https://imgur.com/7b6c5mw.png" height="80%" width="80%" alt="Configuration of OU to Okta"/> 
<img src="https://imgur.com/OZtn85Y.png" height="80%" width="80%" alt="Configuration of AD Agent Complete"/>
<img src="https://imgur.com/Td7EVQw.png" height="80%" width="80%" alt="AD Integration with Okta Complete"/>
<img src="https://imgur.com/I472m11.png" height="80%" width="80%" alt="Verification of Integration Complete. Okta Service Account has been created on AD DS"/>

<p align="center">
<h2>Provision Okta with Active Directory Users</h2>
<p align="center">
<img src="https://imgur.com/pE4ed2q.png" height="80%" width="80%" alt="Configuring Incremental Import of Users to Okta"/>  
<br />
<br />

<p align="center">
<h2>Active Directory Integration with Entra ID:</h2>
<p align="center">
- <b>Download Microsoft Entra Provisioning Agent and Install on AD DS Server</b>
<p align="center">  
- <b>Run Microsoft Entra Provisioning Agent Configuration on AD DS Server</b>
<p align="center">
<img src="https://imgur.com/P08bnMJ.png" height="80%" width="80%" alt="Configuring Service Account"/> 
<img src="https://imgur.com/Wx20NEZ.png" height="80%" width="80%" alt="Connecting Active Directory"/>
<img src="https://imgur.com/40fK90D.png" height="80%" width="80%" alt="Configuration of the Agent"/>
<img src="https://imgur.com/uq3pUwz.png" height="80%" width="80%" alt="Configuration of the Agent"/>
<img src="https://imgur.com/QXv6VzW.png" height="80%" width="80%" alt="Agent Configuration Complete"/>

<p align="center">
<h2>Verification</h2>
<p align="center">
<img src="https://imgur.com/J9aWQeN.png" height="80%" width="80%" alt="Verfication of agent"/>
<img src="https://imgur.com/LmbnYj8.png" height="80%" width="80%" alt="Verification of Azure AD connector"/>

<p align="center">
<h2>Cloud Sync of Active Directory Domain Services</h2>
  <p align="center">
<img src="https://imgur.com/5Y22sCa.png" height="80%" width="80%" alt="Configuring cloud sync"/>  
<img src="https://imgur.com/J1ToUKG.png" height="80%" width="80%" alt="Cloud Sync Configuration"/> 
<img src="https://imgur.com/JLAaYm1.png" height="80%" width="80%" alt="Cloud Sync successful"/> 

<h2>Conclusion:</h2>
This project demonstrated my ability to design and implement a robust Identity and Access Management (IAM) solution by combining on-premises infrastructure with cloud-based services. By building a fully functional lab environment, I reinforced my hands-on experience in configuring Active Directory, deploying critical network services, managing large-scale user and group structures, enforcing group policies, and integrating with modern cloud platforms like Okta and Microsoft Entra ID. The successful synchronization of identities between on-premises and cloud environments highlights my expertise in hybrid identity management, showcasing skills essential for securing and streamlining enterprise-level IAM operations.

