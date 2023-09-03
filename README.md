# azure-network-protocols
<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



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

- Step 0 Create a Microsoft Azure Subscription (Note: credit card needed for free Azure credits)
- Step 1 Create a Resource Group
- Step 2 Create a Windows 10 Virtual Machine (VM), select the previously created Resource Group, allow the VM to create a Virtual 
         Network 
- Step 3 Create a Linux (Ubuntu) VM, select the previously created Resource Group and Vnet
- Step 4 Observe Your Virtual Network within Network Watcher


<h2>Actions and Observations</h2>

<p>

![image](https://github.com/JacobLebron/azure-network-protocols/assets/143144930/47e20ffe-310a-4b9e-b973-68ff701d51f8)


</p>
<p>
While creating the Windows 10 VM, notice that a new Virtual Network (Vnet) and Subnet is created automatically. In order for the Linux VM to communicate with the Windows 10 VM, make sure that both VMs are using both the previously created Resource Group and Vnet.

<h2> Observe ICMP Traffic</h2>

- Step 1 Use Remote Desktop to connect to your Windows 10 Virtual Machine
- Step 2 Within your Windows 10 Virtual Machine, Install Wireshark
- Step 3 Open Wireshark and filter for ICMP traffic only
- Step 4 Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM
- Step 5 Observe ping requests and replies within WireShark
- Step 6 From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (i.e. www.amazon.com)
- Step 7 Observe traffic
- Step 8 Initiate a non-stop ping from VM1 to VM2
- Step 9 Open the Network Security Group that VM2 is using and disable inbound ICMP traffic
- Step 10 Back in the VM1 observe the ICMP traffic in WireShark and the command line Ping activity
- Step 12 Re-enable ICMP traffic for the Network Security Group VM2 is using
- Step 13 Back in VM1, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
- Step 14 Stop the ping activity
  
  
  
  ![image](https://github.com/JacobLebron/azure-network-protocols/assets/143144930/19def467-9d8e-4155-ba66-5fcc69a663af)

<br />

<p> 


       

</p>
<p>
By installing Wireshark, you will be able to inspect traffic between both virtual machines. Before filtering for ICMP traffic only, notice all the spam traffic that happens in the back ground.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
         





         

         
         
         
         
         orem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
