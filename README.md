<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1 - Create resource group and virtual machines through Azure
- Step 2 - Use virtual machine public IP address to boot Remote Desktop Connection
- Step 3 -  Configure Wireshark and Powershell
- Step 4 - Use various protocols and observe network traffic

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Part 1 (Create our Resources)

  
1. Create a Resource Group

2. Create a Windows 10 Virtual Machine (VM). While creating the VM, select the previously created Resource Group
   and allow the VM to create a new Virtual Network (Vnet) and Subnet
   
4. Create a Linux (Ubuntu) VM. While creating the VM, select the previously created Resource Group and Vnet
Observe Your Virtual Network within Network Watcher

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Part 2 (Observe ICMP Traffic)
  
1. Use Remote Desktop to connect to your Windows 10 Virtual Machine. Within your Windows 10 Virtual Machine, Install Wireshark
Open Wireshark and filter for ICMP traffic only

2. Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM
   
3. Observe ping requests and replies within WireShark
From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark

4. Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM

5. Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic

6. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity

7. Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using

8. Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
Stop the ping activity

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
