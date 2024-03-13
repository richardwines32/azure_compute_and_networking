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

</p>
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 36 54 PM" src="https://github.com/richardwines32/DNS/assets/162821778/48ff7798-4c89-43f6-b9da-5d872b54d4c3">
</p>

<br />
<p>
2.  Local DNS Cache Exercise.  Go back to DC-1 and change mainframe’s record address to 8.8.8.8.  

</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 44 15 PM" src="https://github.com/richardwines32/DNS/assets/162821778/12d51939-2004-4714-bc18-7632b227d1ad">

</p>

<br />
<p>
2A.  Go back to Client-1 and ping “mainframe” again.  Observe that it still pings the old address.  
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 47 23 PM" src="https://github.com/richardwines32/DNS/assets/162821778/cd41320b-6a15-424b-9233-4848f7334d9d">

</p>

<br />
<p>
2B.  Observe the local dns cache (ipconfig /displaydns).  
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 52 37 PM" src="https://github.com/richardwines32/DNS/assets/162821778/f6504710-f6cb-4cd1-b759-9e53c825b706">


</p>

<br />
<p>
2C.  Flush the DNS cache (ipconfig /flushdns).  Observe that the cache is empty.  
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 55 02 PM" src="https://github.com/richardwines32/DNS/assets/162821778/bd81d852-f929-4f1f-aab4-a248ffd3efac">

</p>

<br />
<p>
2D.  Attempt to ping “mainframe” again. Observe the address of the new record is showing up.
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 56 09 PM" src="https://github.com/richardwines32/DNS/assets/162821778/9387b286-b4ee-4c67-a513-c2088944b34d">

</p>

<br />
<p>
3.  CNAME Record Exercise.  Go back to DC-1 and create a CNAME record that points the host “search” to “www.google.com”.  
 
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 7 06 47 PM" src="https://github.com/richardwines32/DNS/assets/162821778/a26fa383-10f6-4c7d-99e9-e4f43108f0e9">

</p>

<br />
<p>
Go back to Client-1 and attempt to ping “search”, observe the results of the CNAME record.  Finish.  
</p>
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 7 08 52 PM" src="https://github.com/richardwines32/DNS/assets/162821778/7c64022c-f499-4d6d-aa15-2cd4b9516750">

