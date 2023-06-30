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

- Creat two virtual machines with windows 10 and Ubuntu server
- Connect to VM1 using RD
- Install Wireshack
- Test and Observe various network traffics using wireshack with NSGs

<h2>Actions and Observations</h2>

<p>
  <img width="829" alt="image" src="https://github.com/Akeresuleman/azure-network-protocols/assets/137787129/12862081-f78b-40db-b2f9-24f2423a3e19">
  <img width="601" alt="image" src="https://github.com/Akeresuleman/azure-network-protocols/assets/137787129/0488ed76-80e4-435f-8f3d-5fe86d43c866">

Created two virtual machines with the same vnet, one runing windows 10 called VM1 and the other Linux(ubuntu) Called VM2. Connected vm1 using a RD and used it test various network traffic and connectivity between the vms. From vm1 I downloaded and installed wireshack which I will be using to test and observe the various network traffic and protocol. So i used powershell to ping vm2 private ip to make sure there's connectivity between the two vms. next I tested icmpv4 traffic(Continously ping vm2 private IP) betweeen the vms, which was succesful. while the icmpv4 traffic is still going on I then login to the azure portal and deny icmpv4 traffic coming in to vm2 and observe hom the icmp connection becomes unsuccessful and successful when I allow the Imp connection coming to vm2.
I further tested SSH,DNS traffic from vm1 to vm2
