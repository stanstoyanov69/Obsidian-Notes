
1. First we check if the target is online. After successfully established reply we can proceed with enumeration phase.


```
ping 10.129.67.229

```


2. Enumeration Phase

```
sudo nmap -sV 10.129.67.229  
```

![[Pasted image 20250124185900.png]]

Following the completion of the scan, we have identified port 23/tcp in an open state, running the telnet service. Following a quick Google search of this protocol, we find out that telnet is an old service used for remote management of other hosts on the network. Since the target is running this service, it can receive telnet connection requests from other hosts in the network (such as ourselves). Usually, connection requests through telnet are configured with username/password combinations for increased security.


3.  After identyfing the service on port 23. We managed to establish connection with username: root 

![[Pasted image 20250124190739.png]]