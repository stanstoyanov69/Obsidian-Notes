**Ports** in networking are logical channels or endpoints used to differentiate services or applications running on a networked device (like a computer or server). They are part of the **Transport Layer** (Layer 4) in the OSI model, helping direct traffic between devices based on different types of services or processes.

Each port is associated with a particular service or protocol and allows multiple services to run simultaneously on the same IP address. For example, a computer can be running a web server, email server, and FTP server all at the same time, each using a different port to keep their traffic separate.

|                                                                    |                 |                                                                                                                                                            |
| ------------------------------------------------------------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Protocol**                                                       | **Port Number** | **Description**                                                                                                                                            |
| **F**ile **T**ransfer **P**rotocol (**FTP**)                       | 21              | This protocol is used by a file-sharing application built on a client-server model, meaning you can download files from a central location.                |
| **S**ecure **Sh**ell (**SSH**)                                     | 22              | This protocol is used to securely login to systems via a text-based interface for management.                                                              |
| **H**yper**T**ext Transfer Protocol (**HTTP**)                     | 80              | This protocol powers the World Wide Web (WWW)! Your browser uses this to download text, images and videos of web pages.                                    |
| **H**yper**T**ext **T**ransfer **P**rotocol **S**ecure (**HTTPS**) | 443             | This protocol does the exact same as above; however, securely using encryption.                                                                            |
| **S**erver **M**essage **B**lock (**SMB**)                         | 445             | This protocol is similar to the File Transfer Protocol (FTP); however, as well as files, SMB allows you to share devices like printers.                    |
| **R**emote **D**esktop **P**rotocol (**RDP**)                      | 3389            | This protocol is a secure means of logging in to a system using a visual desktop interface (as opposed to the text-based limitations of the SSH protocol). |
1. **FTP**:
    - Port 20 (FTP data transfer)
    - Port 21 (FTP command control)
2. **SSH**:
    - Port 22
3. **Telnet**:
    - Port 23
4. **SMTP**:
    - Port 25
5. **DNS**:
    - Port 53 (UDP) and Port 53 (TCP)
6. **HTTP**:
    - Port 80
    - Port 443 (HTTPS)
7. **POP3**:
    - Port 110
    - Port 995 (POP3S)
8. **IMAP4**:
    - Port 143
    - Port 993 (IMAPS)
9. **SNMP**:
    - Port 161 (UDP) and Port 162 (UDP)
10. **LDAP**:
    - Port 389 (TCP and UDP)

**Registered Ports (1024-49151)**

1. **RADIUS**:
    
    - Port 1645 (TCP)
    - Port 1646 (UDP)
2. **SMB/CIFS**:
    
    - Port 445 (TCP)
3. **RDP**:
    
    - Port 3389 (TCP)
4. **DHCP**:
    
    - Port 67 (UDP) and Port 68 (UDP)
5. **TFTP**:
    
    - Port 69 (UDP)

**Unofficial Ports**

1. **AOL Instant Messenger**:
    
    - Port 5190 (TCP and UDP)

2. **Tonido Directory Server**:
    
    - Port 24465 (TCP and UDP)

3. **Mosh**:
    
    - Dynamic, private, or ephemeral ports (60000-61000)