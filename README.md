<h1>Azure Compute and Networking</h1>
In this tutorial, we will be working with DNS. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Wireshark


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux (Ubuntu)

<h2>Actions and Observations</h2>
<p>
1.  Part 1 (Create our Resources).  Create a Resource Group.  Create a Windows 10 Virtual Machine (VM).  While creating the VM, select the previously created Resource Group.  While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet.  Create a Linux (Ubuntu) VM.  While creating the VM, select the previously created Resource Group and Vnet.  Observe Your Virtual Network within Network Watcher.


</p>
<p><img width="1512" alt="Screenshot 2024-03-13 at 3 07 10 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/7b0824e2-c132-4e92-b558-347a6efbac77">
<img width="1512" alt="Screenshot 2024-03-13 at 3 10 05 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/f7c9a7ee-5200-486c-b407-6311585fc6f9">
<img width="1512" alt="Screenshot 2024-03-13 at 3 10 50 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/f4fac8cf-9add-4ef3-b7ba-0fa34b6d50f7">
<img width="1512" alt="Screenshot 2024-03-13 at 3 15 01 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/8ee22e77-b2c1-4bea-bfb5-13061d64a5f1">
<img width="1512" alt="Screenshot 2024-03-13 at 3 16 05 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/5c23ee57-90ef-434e-b0e6-52473a407671">
<img width="1512" alt="Screenshot 2024-03-13 at 3 23 49 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/7d09396e-d7e9-4a20-9d4d-dd81b5c4c75e">

 
</p>
<br />
<p>
2.Part 2 (Observe ICMP Traffic).  Use Remote Desktop to connect to your Windows 10 Virtual Machine.  Within your Windows 10 Virtual Machine, Install Wireshark.  Open Wireshark and filter for ICMP traffic only.  Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM.  Observe ping requests and replies within WireShark.  From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark.  Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM.  Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic.  Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity.  Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using.  Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working).  Stop the ping activity.
 
</p> 
<p>
<img width="667" alt="Screenshot 2024-03-13 at 3 31 07 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/93132ed6-99ac-4be5-9813-c3e85c465094">
<img width="1512" alt="Screenshot 2024-03-13 at 3 34 19 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/dfc1befa-4753-435c-920d-4682fcc5ac36">
<img width="1512" alt="Screenshot 2024-03-13 at 3 47 35 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/32661162-72ab-455c-8dab-92ae93b59fa7">
<img width="1512" alt="Screenshot 2024-03-13 at 3 49 27 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/59123d6d-8964-472c-b3f0-df621c37a6a0">
<img width="1512" alt="Screenshot 2024-03-13 at 3 50 01 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/fd3be449-54ff-4685-9a29-b053cdbe50c2">
<img width="1512" alt="Screenshot 2024-03-13 at 3 51 19 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/1fc5adac-1555-4c4f-9255-b2f60e759f26">
<img width="1512" alt="Screenshot 2024-03-13 at 3 58 43 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/bb62255c-3b67-4c36-b7bb-c94fe7bb9098">
<img width="1512" alt="Screenshot 2024-03-13 at 3 59 58 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/c7aa2746-8780-49b1-bd02-200dcac4c292">
<img width="1512" alt="Screenshot 2024-03-13 at 4 00 25 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/ed430844-fd56-4ac4-a4b7-e29f8ec07800">
<img width="1512" alt="Screenshot 2024-03-13 at 4 01 03 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/3c69fb34-be00-4fca-b76f-21fccb89e103">
<img width="1512" alt="Screenshot 2024-03-13 at 4 01 33 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/cd88da74-0efe-4236-9efa-8a4816967e41">
 
</p>

<br />
<p>
3.  Part 3 (Observe SSH Traffic).  Back in Wireshark, filter for SSH traffic only.  From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address).  Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark.  Exit the SSH connection by typing ‘exit’ and pressing [Enter]

<p>
<img width="1512" alt="Screenshot 2024-03-13 at 4 41 56 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/5fddd1dc-e232-4d98-848a-392f296968d8">
<img width="1512" alt="Screenshot 2024-03-13 at 4 44 39 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/cffa03b7-ef08-475f-a37d-76a5f1e290e8">
<img width="1512" alt="Screenshot 2024-03-13 at 4 46 50 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/87d36fe6-349a-40a7-9e6f-5b610bc06431">

</p>

<br />
<p>
4.  Part 4 (Observe DHCP Traffic)  Back in Wireshark, filter for DHCP traffic only.  From your Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew). 
 Observe the DHCP traffic appearing in WireShark.
</p>

<p>
<img width="1512" alt="Screenshot 2024-03-14 at 2 54 58 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/3692df9e-330c-40da-9bc0-8dea49c28dcb">
<img width="1512" alt="Screenshot 2024-03-14 at 3 00 06 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/f60c2993-f4ab-4fce-ba57-bc740243699e">
<img width="1512" alt="Screenshot 2024-03-14 at 3 01 08 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/5cbb2210-27bf-4d79-add4-3c479166454e">

</p>

<br />
<p>
5.  Part 5 (Observe DNS Traffic).  Back in Wireshark, filter for DNS traffic only.  From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com’s IP addresses are.  Observe the DNS traffic being show in WireShark.

</p>
<p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 01 46 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/e84f4293-2429-4f3c-b4a3-4820ac7f9d7b">
<img width="1512" alt="Screenshot 2024-03-14 at 3 02 46 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/6bf06731-c6d9-4608-a1d5-ccf28cd8f2a0">
<img width="1512" alt="Screenshot 2024-03-14 at 3 03 24 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/8a5ea0b7-646c-402c-bf7b-bd19074cb070">
</p>

<br />
<p>
6.  Part 6 (Observe RDP Traffic) Back in Wireshark, filter for RDP traffic only (tcp.port == 3389)*.  Observe the immediate non-stop spam of traffic? Why do you think it’s non-stop spamming vs only showing traffic when you do an activity?  Answer: because the RDP (protocol) is constantly showing you a live stream from one computer to another, therefore traffic is always being transmitted.  Finish.
 
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-14 at 3 10 44 PM" src="https://github.com/richardwines32/azure_compute_and_networking/assets/162821778/f7ae1b08-063c-4c5e-830e-637c2ea49a37">


</p>


