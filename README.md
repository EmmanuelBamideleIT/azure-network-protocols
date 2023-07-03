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

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Section 1: ICMP Traffic

Connect to the Windows 10 VM using Remote Desktop.

Install Wireshark on the Windows 10 VM

Filter Wireshark for ICMP traffic

Ping the Ubuntu VM from the Windows 10 VM and observe the ping requests and replies in Wireshark

Ping a public website (e.g., www.google.com) from the Windows 10 VM and observe the traffic in Wireshark

Initiate a perpetual/non-stop ping from the Windows 10 VM to the Ubuntu VM

Disable incoming (inbound) ICMP traffic in the Network Security Group of the Ubuntu VM

Observe the ICMP traffic in Wireshark and the command line Ping activity from the Windows 10 VM

Re-enable ICMP traffic for the Network Security Group of the Ubuntu VM

Observe the ICMP traffic in Wireshark and the command line Ping activity (should start working)

Stop the ping activity</p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Section 2: SSH Traffic

Filter Wireshark for SSH traffic
SSH into the Ubuntu VM from the Windows 10 VM using the private IP address

Type commands into the SSH connection and observe SSH traffic in Wireshark

Exit the SSH connection</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Section 3: DHCP and DNS Traffic

Filter Wireshark for DHCP traffic

Attempt to renew the Windows 10 VM's IP address using the command line (ipconfig /renew)

Observe the DHCP traffic in Wireshark

Filter Wireshark for DNS traffic

Use nslookup within the Windows 10 VM's command line to obtain IP addresses for google.com and disney.com

Observe the DNS traffic in Wireshark</p>
<br />
