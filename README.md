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
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 25 17 PM" src="https://github.com/richardwines32/DNS/assets/162821778/b9834df5-0199-44c9-899a-5d69ddbd6d27">
 
</p>
<br />
<p>
 1A.  Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address. 
</p> 
<p>
<img width="1512" alt="Screenshot 2024-03-11 at 6 32 54 PM" src="https://github.com/richardwines32/DNS/assets/162821778/ce944376-2469-4a6f-9465-6b47107ca165">
 
</p>

<br />
<p>
1B.  Go back to Client-1 and try to ping it. Observe that it works. 
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

