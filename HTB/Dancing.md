Enumeration

We start, as always, by scanning the target once we are connected to the VPN. Running the following command will make nmap scan all of the ports and display service versions for each of them.


![[Pasted image 20250124222703.png]]

We see that on port 445 there is a microsoft-ds or smbclient running.
We will try to connecto to the smbclient

![[Pasted image 20250124222920.png]]

We see there is a directory called WorkShares. We try to connect with default credentials.

![[Pasted image 20250124223026.png]]

We see the file we needed. 