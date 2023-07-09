<p align="center">
<img width="300" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/e1570b9d-262b-41de-a27a-f1c398a517c6">
</p>

<h1>Observing Network Protocols</h1>
I will use Wireshark to inspect network protocols between a linux (Ubuntu) and windows machine. This will be done using virtual machines in Microsoft Azure. I will use tools like ping, nslookup, ssh in Powershell. The network protocols that will be inspected are DNS, ICMP, DHCP, and SSH. <br />

<h2>Creating Virtual Machines in Azure and Observe ICMP Traffic</h2>

<p>
<img width="612" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/e161012d-34a3-4836-85e8-60db82d64a63">
<P>
  Create a Resource group in Azure. Create windows 10 and Linux (Ubuntu) virtual machines in the same network. Next use Remote Desktop to connect to the windows VM.
</P>
<h2>Installing Wireshark</h2>
<p>
<img width="851" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/d3ac4984-47fd-4999-9c20-9f56ea075e34">
<P>
Download Wireshark in the Windows VM.</p>

<p>
<img width="949" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/626baf03-22c7-4648-b82f-21ed9c015247">
<P>
Open Wireshark and filter for ICMP traffic. Ping the private IP address of the Linux VM. Ping Google.com. If the Windows machine is able to reach and communicate with the Linux machine, it will reply back as shown above. Observe the ICMP traffic in Wireshark.</p>

<h2>Observing SSH Traffic</h2>
<p>
<img width="943" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/1d2097ef-284f-4b83-b21f-d005ac91d98a">
<P>
Filter Wireshark for SSH traffic. Connect to the Linux VM using SSH from the Windows VM. Observe SSH traffic in Wireshark which starts when the SSH connection is made. 

 <h2>Observing DNS Traffic</h2>
<p>
<img width="943" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/5c3b94f9-b71a-4886-b586-00bd38d94bdd">
<P>
Filter Wireshark for DNS traffic. Use nslookup in powershell to find the IP address of Google.com. DNS traffic is generated in Wireshark. 
   
<h2>Observing DHCP Traffic</h2>
<p>
<img width="943" alt="image" src="https://github.com/mmanzoor825/azure-network-protocols/assets/138532574/5c3d1613-46c5-4211-8a3b-39a46b1359fe">
<P>
Filter Wireshark for DHCP traffic. Re-assign Windows VM a new IP address. Observe DHCP traffic in Wireshark.
  
  <br />
