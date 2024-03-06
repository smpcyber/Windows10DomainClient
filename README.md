<h1>Windows 10 Domain Client</h1>

<h2>Description</h2>

Step-by-step process of installing and configuring Windows 10 as a domain workstation to my Windows Server 2019 domain controller lab.  Using Oracle VirtualBox for virtualization, including the extension pack for disk encryption.

<sub><b>**This repository assumes familiarity with virtualization software</b></sub>

<br />
<br />

<p align="center">
<b>[Virtualizing and Installing Windows 10]</b>
<br />
<br />
<img src="https://i.imgur.com/fSKXzRj.png" width="50%" height="50%">
<br />
<sub>From Oracle VM VirtualBox Manager, click "New"</sub>
<br />
<br />
<img src="https://i.imgur.com/ihqWyOB.png" width="50%" height="50%">
<br />
<sub>Name virtual machine
<br />
Select Windows 10 .iso file under "ISO Image"
<br />
Click "Next"</sub>
<br />
<br />
<img src="https://i.imgur.com/jIf82hS.png" width="50%" height="50%">
<br />
<sub>After mounting ISO image, click "Settings"</sub>
<br />
<br />
<img src="https://i.imgur.com/M3KlF0V.png" width="50%" height="50%">
<br />
<sub>Under "Disk Encryption" tab, check "Enable Disk Encryption"
<br />
Enter and confirm disk encryption password</sub>
<br />
<br />
<img src="https://i.imgur.com/jPJD5s0.png" width="50%" height="50%">
<br />
<sub>Under "Network," select "Internal Network" under "Attached to:"
<br />
**This will allow the Windows 10 client to connect to my domain controller</sub>
<br />
<br />
<img src="https://i.imgur.com/Dxffec3.png" width="50%" height="50%">
<br />
<sub>Run Windows 10 virtual machine
<br />
Enter disk encryption password</sub>
<br />
<br />
<img src="https://i.imgur.com/KCKDKwE.png" width="50%" height="50%">
<br />
<sub>Upon starting startup, select language, time and currency, and keyboard/input method
<br />
Click "Next"</sub>
<br />
<br />
<img src="https://i.imgur.com/qVu6RzH.png" width="50%" height="50%">
<br />
<sub>When prompted, enter product key
<br />
**For the purposes of this lab, I clicked "I don't have a product key"</sub>
<br />
<br />
<img src="https://i.imgur.com/1mVlZVf.png" width="50%" height="50%">
<br />
<sub>Installing Windows 10 Pro to be able to connect to domain
<br />
**Home edition does not allow client to be part of a domain</sub>
<br />
<br />
<img src="https://i.imgur.com/pp6Le2X.png" width="50%" height="50%">
<br />
<sub>Custom install for new virtual machine</sub>
<br />
<br />
<b>[Verifying Connection to Domain Controller using Command Prompt]</b>
<br />
<br />
<img src="https://i.imgur.com/0WiJyIG.png" width="50%" height="50%">
<br />
<sub>Upon finishing installation and logging in, search Command Prompt (or cmd)
<br />
Right-click and select "Run as administrator"</sub>
<br />
<br />
<img src="https://i.imgur.com/t5jxZTL.png" width="50%" height="50%">
<br />
<sub>Run command "ipconfig /all"</sub>
<br />
<br />
<img src="https://i.imgur.com/8faLpLv.png" width="50%" height="50%">
<br />
<sub>Verify DHCP, IPv4 address, and Default Gateway are configured</sub>
<br />
<br />
<img src="https://i.imgur.com/l3CzGbk.png" width="50%" height="50%">
<br />
<sub>Verify domain client appears in domain controller's DHCP IPv4 Address Leases
<br />
Verify domain client's IPv4 address has been leased by domain controller's DHCP service</sub>
<br />
<br />
<b>[Verify Connection to Internet Using Command Prompt]</b> 
<br />
<br />
<img src="https://i.imgur.com/pFdCmWk.png" width="50%" height="50%">
<br />
<sub>Ping external website, e.g. "www.google.com"
<br />
Verify client successfully pings server</sub>
<br />
<br />
<b>[Renaming Domain Client and Joining Domain]</b>
<br />
<br />
<img src="https://i.imgur.com/m5LaJuZ.png" width="50%" height="50%">
<br />
<sub>Right-click Start charm
<br />
Select "System"</sub>
<br />
<br />
<img src="https://i.imgur.com/cfXUHF0.png" width="50%" height="50%">
<br />
<sub>Click "Rename this PC (advanced)" under "About"</sub>
<br />
<br />
<img src="https://i.imgur.com/6eDOxBV.png" width="50%" height="50%">
<br />
<sub>Under System Properties, click "Change"</sub>
<br />
<br />
<img src="https://i.imgur.com/gjlf2Et.png" width="50%" height="50%">
<br />
<sub>Enter new computer name if desired
<br />
Select "Member of"
<br />
Enter domain name of domain controller
<br />
**My domain is called zenith.com</sub>
<br />
<br />
<img src="https://i.imgur.com/paiVIpG.png" width="50%" height="50%">
<br />
<sub>Enter domain administrator credentials</sub>
<br />
<br />
<img src="https://i.imgur.com/IgwzvJE.png" width="50%" height="50%">
<br />
<sub>Verify domain client has successfully joined domain</sub>
<br />
<br />
<img src="https://i.imgur.com/dHOQHYn.png" width="50%" height="50%">
<br />
<sub>When prompted, restart domain client</sub>
<br />
<br />
<img src="https://i.imgur.com/cwqY5ON.png" width="50%" height="50%">
<br />
<sub>Domain client is now able to be accessed by Active Directory users created in Windows Server 2019 lab</sub>
<br />
<br />

</p>
