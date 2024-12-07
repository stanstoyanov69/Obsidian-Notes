### What is Port Scanning?

Port scanning is a method of determining which ports on a network are open and could be receiving or sending data. It is also a process for sending packets to specific ports on a host and analyzing responses to identify vulnerabilities. 

### How can you define Blue Team and Red Team basically?

Red team is attacker side, blue team is defender side.

### What is Firewall?

Firewall is a device that allows or blocks the network traffic according to the rules.
### Explain Security Misconfiguration

It is a security vulnerability caused by incomplete or incorrect misconfiguration.
### Explain Vulnerability, Risk and Threat

**Vulnerability:** Weakness in an information system, system security procedures, internal controls, or implementation that could be exploited or triggered by a threat source. (src: [NIST](https://csrc.nist.gov/glossary/term/vulnerability))

**Risk:** The level of impact on agency operations (including mission functions, image, or reputation), agency assets, or individuals resulting from the operation of an information system given the potential impact of a threat and the likelihood of that threat occurring. (src: [NIST](https://csrc.nist.gov/glossary/term/security_risk))

**Threat:** Any circumstance or event with the potential to adversely impact organizational operations, organizational assets, individuals, other organizations, or the Nation through a system via unauthorized access, destruction, disclosure, modification of information, and/or denial of service. (src: [NIST](https://csrc.nist.gov/glossary/term/cyber_threat))
### What is compliance?

Following the set of standards authorized by an organization, independent part, or government.
### What is MITRE ATT&CK?

MITRE ATT&CK® is a globally-accessible knowledge base of adversary tactics and techniques based on real-world observations. The ATT&CK knowledge base is used as a foundation for the development of specific threat models and methodologies in the private sector, in government, and in the cybersecurity product and service community.
### What is CIA triad?
**Confidentiality:** Confidentiality involves the efforts of an organization to make sure data is kept secret or private. A key component of maintaining confidentiality is making sure that people without proper authorization are prevented from accessing assets important to your business.

**Integrity:** Integrity involves making sure your data is trustworthy and free from tampering. The integrity of your data is maintained only if the data is authentic, accurate, and reliable.

**Availability:** Systems, networks, and applications must be functioning as they should and when they should. Also, individuals with access to specific information must be able to consume it when they need to, and getting to the data should not take an inordinate amount of time.
### What is AAA?

**Authentication:** Authentication involves a user providing information about who they are. Users present login credentials that affirm they are who they claim. ([Fortinet](https://www.fortinet.com/resources/cyberglossary/aaa-security))

**Authorization:** Authorization follows authentication. During authorization, a user can be granted privileges to access certain areas of a network or system. ([Fortinet](https://www.fortinet.com/resources/cyberglossary/aaa-security))

**Accounting:** Accounting keeps track of user activity while users are logged in to a network by tracking information such as how long they were logged in, the data they sent or received, their Internet Protocol (IP) address, the Uniform Resource Identifier (URI) they used, and the different services they accessed. ([Fortinet](https://www.fortinet.com/resources/cyberglossary/aaa-security))
### What is Cyber Kill Chain?

Developed by Lockheed Martin, **the Cyber Kill Chain®** framework is part of the [**Intelligence Driven Defense®**](https://www.lockheedmartin.com/en-us/capabilities/cyber/intelligence-driven-defense.html) model for identification and prevention of cyber intrusions activity. The model identifies what the adversaries must complete in order to achieve their objective.

The seven steps of the Cyber Kill Chain® enhance visibility into an attack and enrich an analyst’s understanding of an adversary’s tactics, techniques and procedures. ([Lockheed Martin](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html))
- Reconnaissance
- Weaponization
- Delivery
- Exploitation
- Installation
- Command & Control
- Actions on Objectives
### What is OSI Model? Explain each layer.

The **Open Systems Interconnection** (**OSI**) **Model** is a conceptual model that describes the universal standard of communication functions of a telecommunication system or computing system, without any regard to the system's underlying internal technology and specific protocol suites. ([Wikipedia](https://en.wikipedia.org/wiki/OSI_model))

![OSI Model](https://cdn.prod.website-files.com/647e4e328280afb2dff45d0e/65f9f2db1982a87b79fc275b_68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f3437382f312a78577254444f6a4b3852646f673934374c66367746672e706e67.png)

1. **Physical Layer:** The Physical Layer is responsible for the transmission and reception of unstructured raw data between a device, such as a network interface controller, Ethernet hub or network switch and a physical transmission medium. It converts the digital bits into electrical, radio, or optical signals.
2. **Data Link Layer:** The Data Link Layer provides node-to-node data transfer a link between two directly connected nodes. It detects and possibly corrects errors that may occur in the physical layer. It defines the protocol to establish and terminate a connection between two physically connected devices. It also defines the protocol for flow control between them. IEEE 802 divides the Data Link Layer into two sublayers:
    - [Medium Access Control](https://en.wikipedia.org/wiki/Medium_access_control) (MAC) Layer – responsible for controlling how devices in a network gain access to a medium and permission to transmit data.
    - [Logical Link Control](https://en.wikipedia.org/wiki/Logical_link_control) (LLC) Layer – responsible for identifying and encapsulating network layer protocols, and controls error checking and frame synchronization.
3. **Network Layer:** The Network Layer provides the functional and procedural means of transferring packets from one node to another connected in "different networks".
4. **Transport Layer:** The Transport Layer provides the functional and procedural means of transferring variable-length data sequences from a source host to a destination host from one application to another across a network, while maintaining the Quality of Service (QoS) functions. Transport protocols may be connection-oriented or connectionless.
5. **Session Layer:** The Session Layer creates the setup, controls the connections, and ends the teardown, between two or more computers, which is called a "session". Since DNS and other Name Resolution Protocols operate in this part of the layer, common functions of the session layer include user logon (establishment), name lookup (management), and user logoff (termination) functions. Including this matter, authentication protocols are also built into most client software, such as FTP Client and NFS Client for Microsoft Networks. Therefore, the session layer establishes, manages and terminates the connections between the local and remote application.
6. **Presentation Layer:** The Presentation Layer establishes data formatting and data translation into a format specified by the application layer during the encapsulation of outgoing messages while being passed down the protocol stack, and possibly reversed during the deencapsulation of incoming messages when being passed up the protocol stack. For this very reason, outgoing messages during encapsulation are converted into a format specified by the application layer, while the conversation for incoming messages during deencapsulation are reversed.
7. **Application layer:** The Application Layer is the layer of the OSI model that is closest to the end user, which means both the OSI application layer and the user interact directly with software application that implements a component of communication between the client and server, such as File Explorer and Microsoft Word. Such application programs fall outside the scope of the OSI model unless they are directly integrated into the Application layer through the functions of communication, as is the case with applications such as Web Browsers and Email Programs. Other examples of software are Microsoft Network Software for File and Printer Sharing and Unix/Linux Network File System Client for access to shared file resources.

### What is Three-Way Handshake?

![enter image description here](https://cdn.prod.website-files.com/647e4e328280afb2dff45d0e/65f9f2db63c58ae0b5e9a874_68747470733a2f2f756d7574746f73756e2e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031392f30392f39345f73796e5f666967315f6c672e6a7067.jpeg)

TCP uses a three-way handshake to establish a reliable connection. The connection is full duplex, and both sides synchronize (SYN) and acknowledge (ACK) each other.

The client chooses an initial sequence number, set in the first SYN packet. The server also chooses its own initial sequence number, set in the SYN/ACK packet.

Each side acknowledges each other's sequence number by incrementing it; this is the acknowledgement number. The use of sequence and acknowledgment numbers allows both sides to detect missing or out-of-order segments.

Once a connection is established, ACKs typically follow for each segment. The connection will eventually end with a RST (reset or tear down the connection) or FIN (gracefully end the connection). ([ScienceDirect](https://www.sciencedirect.com/topics/computer-science/three-way-handshake))
### What is DHCP?

The **Dynamic Host Configuration Protocol** (DHCP) is a network management protocol used on Internet Protocol (IP) networks for automatically assigning IP addresses and other communication parameters to devices connected to the network using a client–server architecture.
### What is ARP?

The **Address Resolution Protocol** (**ARP**) is a communication protocol used for discovering the Data Link Layer address, such as a MAC address, associated with a given Network Layer address, typically an IPv4 address. This mapping is a critical function in the Internet protocol suite. ([Wikipedia](https://en.wikipedia.org/wiki/Address_Resolution_Protocol))

### What are Encoding, Hashing, Encryption?

**Encoding:** Converts the data in the desired format required for exchange between different systems.

**Hashing:** Maintains the integrity of a message or data. Any change did any day could be noticed.

**Encryption:** Ensures that the data is secure and one needs a digital verification code or image in order to open it or access it.
### What are differences between Hashing and Encryption?

**Hashing:** Hashing is the process of converting the information into a key using a hash function. The original information cannot be retrieved from the hash key by any means. ([GeeksforGeeks](https://www.geeksforgeeks.org/difference-between-hashing-and-encryption/))

**Encryption:** Encryption is the process of converting a normal readable message known as plaintext into a garbage message or not readable message known as Ciphertext. The ciphertext obtained from the encryption can easily be transformed into plaintext using the encryption key. ([GeeksforGeeks](https://www.geeksforgeeks.org/difference-between-hashing-and-encryption/))

**Differences:**

- The hash function does not need a key to operate.
- While the length of the output can variable in encryption algorithms, there is a fixed output length in hashing algorithms.
- Encryption is a two-way function that includes encryption and decryption whilst hashing is a one-way function that changes a plain text to a unique digest that is irreversible.

## Cyber Security Interview Questions for Freshers

### 1. Define Cybersecurity?

In general, we can say that Cyber Security deals with protecting digital systems, networks, and data from unauthorized access, cyberattacks, and malicious activities. The main goal of cybersecurity is to safeguard the system from various threats, including viruses, malware, ransomware, phishing, and insider threats. To achieve this goal, it implements practices like encryption, firewalls, intrusion detection systems (IDS), vulnerability assessments, and security awareness training. 

|   |
|---|
|**Gain essential skills to defend your organization from security threats by enrolling in our [Cyber Security Training](https://mindmajix.com/cyber-security-training "Cyber Security Training").**|

### 2. What is Cryptography?

Cryptography is a method to transform and transmit confidential data in an encoded way to protect the information from third parties for whom data is not authorized. It involves the transformation of plaintext (unencrypted data) into ciphertext (encrypted data) using mathematical algorithms and cryptographic techniques.

### 3. How does the Encryption Work? 

Encryption works by converting plaintext data into ciphertext using encryption algorithms and keys. The encryption process scrambles the original data which makes it unreadable to unauthorized users. To decrypt the ciphertext and retrieve the original data, the recipient uses a decryption key. Hence, the data can be communicated between the systems confidentially. 

### 4. What is the difference between Threat, Vulnerability, and Risk?

**Threat:** It is the factor with the potential to cause harm by damaging or destroying the official data of a system or organization. For example, a Distributed Denial of Service (DDoS) attack is a threat where attackers flood a network or server with excessive traffic, causing it to become unavailable to legitimate users.

**Vulnerability:** It refers to weaknesses in a system that makes threat outcomes more possible and even more dangerous. An example of a vulnerability is outdated software that hasn't been patched against known security vulnerabilities.

**Risk:** It refers to a combination of threat probability and impact/loss. In simple terms, it is related to potential damage or loss when a threat exploits the vulnerability. The Risk is calculated using the Threat probability and Potential loss. 

_Risk = Threat probability * Potential loss_ 

### 

### 5. What are the latest tools and frameworks for Cyber Security?

Below are the top tools along with later versions that you must be aware about during your Cyber Security Interview. 

- **Metasploit:** It is the penetration testing framework for finding and exploiting vulnerabilities in systems. Its latest version for the Metasploit Pro is 4.22.2. 
- **John the Ripper:**  This is a password-cracking tool used to detect weak passwords and hash encryption. Its latest jumbo version is 1.9.0.
- **Wireshark:** it is the network protocol analyzer that captures and inspects data packets on a network. Its latest stable release is 4.2.4.  
- **NetStumbler:** It comes as the wireless network scanner for Windows systems with the latest version 0.4.0. 
- **Forcepoint:** It is a renowned cybersecurity company offering solutions for data protection and threat intelligence.
- **Aircrack-ng:** This is the complete suite of wireless network security tools for assessing Wi-Fi security. Its latest version is 1.7. 

### 6. What is the difference between IDS and IPS?

|   |   |
|---|---|
|**Intrusion Detection Systems (IDS)**|**Intrusion Prevention Systems (IPS)**|
|It only detects intrusions but is unable to prevent intrusions.|It detects and prevents intrusions.|
|It's a monitoring system.|It’s a control system.|
|It needs a human or another system to look at the results.|It needs a regularly updated database with the latest threat data.|

### 7. What is a Botnet?

 A Botnet is a group of internet-connected devices such as servers, PCs, mobile devices, etc., that are affected and controlled by malware.

It is used for stealing data, sending spam, performing distributed denial-of-service attack (DDoS attack), and more, and also to enable the user to access the device and its connection.

### 8. What is a CIA triad?

 CIA (confidentiality, integrity, and availability) triad is a model designed to handle policies for information security within an organization.

- **Confidentiality -** A collection of rules that limits access to information.
- **Integrity -** It assures the information is trustworthy and reliable.
- **Availability -** It provides reliable access to data for authorized people.

### 9. Symmetric Vs Asymmetric encryption.

|   |   |   |
|---|---|---|
|**Purpose**|**Symmetric Encryption**|**Asymmetric Encryption**|
|**Encryption:**|Uses a single key to encrypt and decrypt information.|Uses a pair of public and private keys to encrypt and decrypt information.|
|**Speed:**|Symmetric encryption performs faster|Asymmetric encryption performs slower compared to symmetric encryption.|
|**Algorithms:**|AES, RC4, DES, QUAD, 3DES, Blowfish, etc.|Diffie-Hellman and RSA|
|**Purpose:**|Preferred for transferring huge data|Mostly used for exchanging secret keys safely.|

### 10. What is the difference between hashing and encryption?

 Both hashing and encryption are used to convert readable data into an unreadable format. The significant difference is that encrypted data can be transformed into original data by decryption, whereas hashed data cannot be processed back to the original data.

### 11. What is two-factor authentication and how it can be implemented for public websites?

- Tw0-factor authentication is also referred to as dual-factor authentication or two-step verification where the user provides two authentication factors for protecting both user credentials and resources while accessing. 
- The two-factor authentication can be implemented on public websites such as Twitter, Microsoft, LinkedIn, and more for enabling another protection on your already protected account with a password.
- For enabling this double factor authentication, you can easily go to settings and then manage security settings.

|   |
|---|
|**Related Article: [Cyber Security Frameworks](https://mindmajix.com/cyber-security-frameworks "Cyber Security Frameworks")**|

### 12. What is the use of a firewall and how it can be implemented?

 A firewall is a security system used to control and monitor network traffic. It is used for protecting the system/network from malware, viruses, worms, etc., and secures unauthorized access from a private network.

The steps required to set up and configure the firewall are listed below: 

- Change the default password for a firewall device.
- Disable the remote administration feature.
- Configure port forwarding for specific applications to function correctly, such as an FTP server or a web server.
- Firewall installation on a network with an existing DHCP server can cause errors unless its firewall’s DHCP is disabled. 
- Make sure the firewall is configured to robust security policies.

[![MindMajix YouTube Channel](https://mindmajix.com/_next/image?url=https%3A%2F%2Fcdn.mindmajix.com%2Fblog%2Fimages%2Fyoutube-banner-ultimate-version.png&w=1920&q=75)](https://bit.ly/3if9dmk "Subscribe MindMajix YouTube Channel")

### 13. What is the difference between vulnerability assessment and penetration testing?

- The terms Vulnerability assessment and penetration testing are both different, but serve an essential function of protecting the network environment.
- Vulnerability Assessment: It’s a process to define, detect, and prioritize the vulnerabilities in computer systems, network infrastructure, applications, etc., and gives the organization the required information to fix the flaws. 
- Penetration Testing: It is also called pen testing or ethical hacking. It’s a process of testing a network, system, application, etc. to identify vulnerabilities that attackers could exploit. In the context of web application security, it is most widely used to augment a web application firewall (WAF).

### 14. What is the difference between stored and reflected XSS?

- **Stored XSS Attacks -** The attacks where the injected scripts are stored on the target servers permanently. In this, the victim retrieves the malicious script from the server when requests the stored information.
- **Reflected XSS Attacks -** In this, the user has to send the request first, then it will start running on the victim’s browser and reflects results from the browser to the user who sent the request.

### 15. What is a three-way handshake process?

A three-way handshake process is used in TCP (Transmission Control Protocol) network for the transmission of data in a reliable way between the host and the client.

It’s called a three-way handshake because three segments are exchanged between the server and the client. 

- **SYN:** The client wants to establish a connection with the server, and sends a segment with SYN(Synchronize Sequence Number) to the server if the server is up and has open ports.
- **SYN + ACK:** The server responds to the client request with SYN-ACK signal bits set if it has open ports.
- **ACK:** The client acknowledges the response of a server and sends an ACK(Acknowledgment) packet back to the server.

|   |
|---|
|**Learn [Cyber Security Training in Bangalore](https://mindmajix.com/cyber-security-training-bangalore "Cyber Security Training in Bangalore")**|

### 16. What are the techniques used in preventing a Brute Force Attack?

A brute Force Attack is a trial and error method that is employed for application programs to decode encrypted data such as data encryption keys or passwords using brute force rather than intellectual strategies. It’s a way to identify the right credentials by repetitively attempting all the possible methods.

Brute Force attacks can be avoided by the following practices:

- Adding password complexity: Include different formats of characters to make passwords stronger.
- Limit login attempts: set a limit on login failures.
- Two-factor authentication: Add this layer of security to avoid brute-force attacks.

## Cyber Security Interview Questions for Experienced

### 17. List the common types of cybersecurity attacks.

The following are the most common types of cybersecurity attacks:

- Denial-of-Service (DoS): Overloading websites or networks to make them crash and stop working.
- Man-in-the-Middle Attacks: Secretly listening in on conversations between people or computers to steal information.
- Credential Reuse: Using the same usernames and passwords across different accounts to break into them.
- Phishing: Tricking people into giving away their personal info, like passwords or credit card numbers, through fake emails or websites.
- Session Hijacking: Taking control of someone's online session to pretend to be them and access their stuff.
- Malware: Bad software that harms your computer or steals your information.
- SQL Injection Attack: Tricking websites to do things they shouldn't, like messing with their databases.
- Cross-site scripting (XSS): Sneaking bad code into websites to steal info from users or make them do things they don't want to.

### 18 Define data leakage and its types.

Data Leakage refers to the illegal transmission of data to an external destination or unauthorized entity within an organization. It can transfer data either physically or electronically. It usually occurs via the web, emails, and mobile data storage devices.

Types of data leakage:

1. **The Accidental Breach -** The majority of data leakage incidents are accidental.
2.  **Ex:** An entity may choose the wrong recipient while sending confidential data.
3. **The Disgruntled or ill-intentioned Employee -** The authorized entity sends confidential data to an unauthorized body. 
4. **Electronic Communications with Malicious Intent -** The problem is all electronic mediums are capable of file transferring and external access sources over the internet.

### 19. What is the use of a Traceroute?

A Traceroute is a network diagnostic tool, used for tracking the pathway of an IP network from source to destination. It records the period of each hop the packet makes while its route to its destination.

### 20. How to prevent CSRF attacks?

CSRF is referred to as Cross-site Request Forgery, where an attacker tricks a victim into performing actions on their behalf.

CSRF attacks can be prevented by using the following ways:

- Employing the latest antivirus software which helps in blocking malicious scripts.
- While authenticating to your banking site or performing any financial transactions on any other website do not browse other sites or open any emails, which helps in executing malicious scripts while being authenticated to a financial site.
- Never save your login/password within your browser for financial transactions.
- Disable scripting in your browser.

|   |
|---|
|**Related Article: [Cyber Attacks and Preventions Methods](https://mindmajix.com/cyber-security-interview-questions "Cyber Attacks and Preventions Methods")**|

### 21. What is port scanning?

A port scanning is an application designed for identifying open ports and services accessible on a host network. Security administrators mostly utilize it for exploiting vulnerabilities, and also by hackers for targeting victims.

Some of the most popular port scanning techniques are listed below:

- Ping scan
- TCP connect
- TCP half-open
- Stealth scanning – NULL, FIN, X-MAS
- UDP

### 22. What is the need for DNS monitoring?

- DNS (Domain Name System) is a service that is used for converting user-friendly domain names into a computer-friendly IP address. It allows websites under a particular domain name that is easy to remember.
- DNS monitoring is nothing but monitoring DNS records to ensure does it route traffic properly to your website, electronic communication, services, and more.

### 23. What is the difference between hashing and salting?

- Hashing is majorly used for authentication and is a one-way function where data is planned to a fixed-length value.
- Salting is an extra step for hashing, where it adds additional value to passwords that change the hash value created.

### 24. How to prevent a ‘Man-in-the-Middle Attack’?

The following practices prevent the ‘Man-in-the-Middle Attacks’:

- Have stronger WAP/WEP Encryption on wireless access points avoids unauthorized users.
- Use a VPN for a secure environment to protect sensitive information. It uses key-based encryption.
- Public key pair-based authentication must be used in various layers of a stack for ensuring whether you are communicating the right things are not.
- HTTPS must be employed for securely communicating over HTTP through the public-private key exchange.

### 25. What are the common methods of authentication for network security? 

- **Biometrics -** It is a known and registered physical attribute of a user specifically used for verifying their identity. 
- **Token -** A token is used for accessing systems. It makes it more difficult for hackers to access accounts as they have long credentials.
- **Transaction Authentication -** A one-time pin or password is used in processing online transactions through which they verify their identity.
- **Multi-Factor Authentication -**  It’s a security system that needs more than one method of authentication.
- **Out-of-Band Authentication -** This authentication needs two different signals from two different channels or networks. It prevents most of the attacks from hacking and identity thefts in online banking.

|   |
|---|
|**Related Article: [Cyber Security Career Path](https://mindmajix.com/cyber-security-career-path "Cyber Security Career Path")**|

### 26. Which is more secure SSL or HTTPS?

- SSL (Secure Sockets Layer) is a secure protocol that provides safer conversations between two or more parties across the internet. It works on top of the HTTP to provide security.
- HTTPS (Hypertext Transfer Protocol Secure) is a combination of HTTP and SSL to provide a safer browsing experience with encryption.
- In terms of security, SSL is more secure than HTTPS.

### 27. What is the difference between black hat, white hat, and grey hat hackers? 

- A black-hat hacker is a person who tries to obtain unauthorized access into a system or a network to steal information for malicious purposes.
- White-hat hackers are also known as ethical hackers; they are well-versed with ethical hacking tools, methodologies, and tactics for securing organization data. They try to detect and fix vulnerabilities and security holes in the systems. Many top companies recruit white hat hackers.
- A grey hat hacker is a computer security expert who may violate ethical standards or rules sometimes but does not have the malicious intent of a black hat hacker.

### 28. What is cognitive security?

Cognitive security is one of the applications of AI technologies that is used explicitly for identifying threats and protecting physical and digital systems based on human understanding processes.

Self-learning security systems use pattern recognition, natural language processing, and data mining to mimic the human brain.

### 

### 29. What is phishing and how it can be prevented?

Phishing is a malicious attempt of pretending oneself as an authorized entity in electronic communication for obtaining sensitive information such as usernames, passwords, etc. through fraudulent messages and emails.

The following practices can prevent phishing:

- Use firewalls on your networks and systems.
- Enable robust antivirus protection that has internet security.
- Use two-factor authentication wherever possible
- Maintain adequate security.
- Don't enter sensitive information such as financial or digital transaction details on web pages that you don't trust.
- Keep yourself updated with the latest phishing attempts.

### 30. What is SQL injection and how it can be prevented?

SQL Injection (SQLi) is a type of code injection attack where it manages to execute malicious SQL statements to control a database server behind a web application. Attackers mostly use this to avoid application security measures and thereby access, modify, and delete unauthorized data.

The following ways will help you to mitigate or prevent SQL injection attacks:

- Include Prepared Statements (with Parameterized Queries)
- Use Stored Procedures
- Validate user input
- Hide data from the error message
- Update your system
- Store database credentials separate and encrypted
- Disable shell and any other functionalities you don’t need

|   |
|---|
|**Visit here to learn [Cyber Security Training in Hyderabad](https://mindmajix.com/cyber-security-training-hyderabad "Cyber Security Training Hyderabad")**|

### 31. How will you keep yourself updated with the latest cybersecurity news?

The following ways will help you to keep up with the latest cybersecurity updates:

- Follow news websites and blogs from security experts. 
- Browse security-related social media topics.
- Check vulnerability alert feeds and advisory sites.
- Attend cybersecurity live events.

### 32. What is a DDOS attack and how to stop and prevent them?

A DDOS (distributed denial-of-service ) is a malicious attempt of disrupting regular traffic of a network by flooding with a large number of requests and making the server unavailable to the appropriate requests. The requests come from several unauthorized sources and hence called distributed denial of service attacks.

The following methods will help you to stop and prevent DDOS attacks:

- Build a denial of service response plan
- Protect your network infrastructure
- Employ basic network security
- Maintain strong network architecture
- Understand the Warning Signs
- Consider DDoS as a service

### 33. What is Cross-Site Scripting and how it can be prevented?

Cross-site scripting is also known as a client-side injection attack, which aims at executing malicious scripts on a victim’s web browser by injecting malicious code.

- The following practices can prevent Cross-Site Scripting:
- Encoding special characters
- Using XSS HTML Filter
- Validating user inputs
- Using Anti-XSS services/tools

## Frequently Asked Cyber Security Interview Questions 

### 33. What do you understand by compliance in Cybersecurity?

- Compliance means living by a set of standards set by an organization/government/independent party. 
- It helps in defining and achieving IT targets and also in mitigating threats through processes like vulnerability management.

### 34. What is the use of Patch Management?

- The purpose of patch management is to keep updating various systems in a network and protect them against malware and hacking attacks.
- Many enterprise patch management tools manage the patching process by installing or deploying agents on a target computer, and they provide a link between centralized patch servers and computers to be patched.

### 35. What is the difference between a false positive and a false negative in IDS?

- A false positive is considered to be a false alarm and a false negative is considered to be the most complicated state.
- A false positive occurs when an IDS fires an alarm for legitimate network activity.
- A false negative occurs when IDS fails to identify malicious network traffic.

Compared to both, a false positive is more acceptable than a false negative as they lead to intrusions without getting noticed.

|   |
|---|
|**Related Article: [Top 10 Cybersecurity Tools In 2020](https://mindmajix.com/cybersecurity-tools "Top 10 Cybersecurity Tools In 2020")**|

### 36 what is the difference between the Red Team and the Blue team?

- The red team and blue team refer to cyberwarfare. Many organizations split the security team into two groups as red team and blue team.
- The red team refers to an attacker who exploits weaknesses in an organization's security.
- The blue team refers to a defender who identifies and patches vulnerabilities into successful breaches.

### 37. Explain System hardening?

- Generally, system hardening refers to a combination of tools and techniques for controlling vulnerabilities in systems, applications, firmware, and more in an organization. 
- The purpose of system hardening is to decrease the security risks by reducing the potential attacks and condensing the system’s attack surface.

The following are the various types of system hardening:

1. Database hardening
2. Operating system hardening
3. Application hardening
4. Server hardening
5. Network hardening

### 38. What is a cybersecurity risk assessment?

A cybersecurity risk assessment refers to detecting the information assets that are prone to cyber-attacks(including customer data, hardware, laptop, etc.) and also evaluates various risks that could affect those assets.

It is mostly performed to identify, evaluate, and prioritize risks across organizations.

The best way to perform cybersecurity risk assessment is to detect:

- Relevant threats in your organization 
- Internal and external vulnerabilities 
- Evaluate vulnerabilities impact if they are exploited

### 39. What are the seven layers of the OSI model?

The main objective of the OSI model is to process the communication between two endpoints in a network.

The seven open systems interconnection layers are listed below:

- **Application layer (layer 7) -** It allows users to communicate with network/application whenever required to perform network-related operations. 
- **Presentation layer (layer 6) -** It manages encryption and decryption of data required for the application layer. It translates or formats data for the application layer based on the syntax of the application that accepts.
- **Session layer (layer 5) -** It determines the period of a system that waits for other applications to respond.
- **Transport layer (layer 4) -** It is used for sending data across a network and also offers error checking practices and data flow controls.
- **Network layer (layer 3) -** It is used to transfer data to and fro through another network.
- **Data-link layer (layer 2) -** It handles the flow of data to and fro in a network. It also controls problems that occur due to bit transmission errors.
- **Physical layer (layer 1) -** It transfers the computer bits from one device to another through the network. It also controls how physical connections are set up to the network and also bits represented into signals while transmitting either optically, electrically, or radio waves.

### 40. How to reset or remove the BIOS password?

There are many ways to reset or remove the BIOS password:

- By removing the CMOS battery
- By using software
- By using the MS-DOS command
- By using motherboard jumper
- By using Backdoor BIOS password

|   |
|---|
|**Related Article: [How to Become a Cyber Security Engineer](https://mindmajix.com/how-to-become-a-cyber-security-engineer "How to Become a Cyber Security Engineer")**|

### 41. What is the use of Address Resolution Protocol (ARP)?

ARP is a protocol specifically used to map IP network addresses to physical addresses, such as Ethernet addresses.

It translates 32-bits addresses to 48-bits addresses and vice versa. This is needed because the most common level of internet protocol(IP) we use today is 32-bits long and MAC addresses are 48-bits long.

### 42. How to protect data in transit Vs rest?

|   |   |   |
|---|---|---|
|**Description**|**Data in Transit**|**Data in Rest**|
|Definition of data|Here data moves actively from one location to another across the internet or private network.|Here data is not transferred from one location to another as data is stored on hard drives, flash drives, etc.|
|Encryption in data protection|It encrypts sensitive data before sending or using encrypted connections(SSL, HTTPS, TLS, etc.)|It encrypts sensitive files before storing or choosing the encrypted storage drive itself.|

### 43. What are the several indicators of compromise(IOC) that organizations should monitor?

The key indicators of compromise that organizations should monitor are listed below:

- Unusual Outbound Network Traffic
- HTML Response Sizes
- Geographical Irregularities
- Increases in Database Read Volume
- Log-In Red Flags
- Unexpected Patching of Systems
- Large Numbers of Requests for the Same File
- Web Traffic with Unhuman Behavior
- Suspicious Registry or System File Changes
- Unusual DNS Requests
- Mobile Device Profile Changes
- Bundles of Data in the Wrong Place
- Mismatched Port-Application Traffic
- Signs of DDoS Activity
- Anomalies in Privileged User Account Activity

### 44. What is Remote Desktop Protocol (RDP)?

- RDP (Remote Desktop Protocol) is a Microsoft protocol specifically designed for application data transfer security and encryption between client devices, users, and a virtual network server.
- It allows administrators to remotely evaluate and resolve issues individual subscribers encounter.
- It supports up to 64,000 separate data channels with a provision for multipoint transmission.

### 45. What is the difference between Diffie Hellman and RSA? 

- **Diffie-Helman:** It’s a key exchange protocol where two parties exchange a shared key that either one can use to encrypt/decrypt messages between them.
- **RSA:** It’s asymmetric key encryption where it has two different keys. The public key can be given to anyone and decrypted with another, which is kept private.

|   |
|---|
|**Related Article: [Cyber Security Best Practices](https://mindmajix.com/top-10-cybersecurity-best-practices "Cyber Security Best Practices")**|

### 46. What is Forward Secrecy and how does it work? 

- Forward secrecy is a feature of specific key agreement protocols which gives assurance that even if the private key of the server is compromised the session keys will not be compromised. It is also known as perfect forward secrecy(PFS).
- The Algorithm that helps in achieving this is called "Diffie–Hellman key exchange".

### 47. What is an active reconnaissance? 

- Active reconnaissance is a kind of computer attack where an intruder engages the target system for collecting data about vulnerabilities.
- The attackers mostly use port scanning to identify vulnerable ports and then exploit the vulnerabilities of services that are associated with open ports.

|   |
|---|
|**Leave an Inquiry to learn [Cyber Security Training in Houston](https://mindmajix.com/cyber-security-training-houston)**|

### 48. What is security misconfiguration?

Security misconfiguration is a vulnerability that could happen if an application/network/device is susceptible to attack due to an insecure configuration option. It can be as simple as keeping the default username/password unchanged.

### 49. What is the difference between information protection and information assurance?

- **Information protection:** It protects the data using encryption, security software, etc., from unauthorized access.
- **Information Assurance:** It keeps the data reliable by ensuring availability, authentication, confidentiality, etc.

### 50. What do you mean by Chain of Custody?

- Chain of custody refers to the probability of data provided as originally acquired and has not been changed before admission into evidence.
- In legal terms, it’s a chronological documentation/paper trail that records a proper sequence of custody, control, analysis, and disposition of electronic or physical evidence.

### 51. What is a zero-day vulnerability? 

A zero-day vulnerability is a software security flaw that is unknown to the vendor or developer and has not yet been patched or fixed. Attackers use these vulnerabilities before the software's developer becomes aware of them. That is why it is called "zero-day," as there are zero days of advance notice to avoid the risk.

### 52. How does a Secure Socket Layer (SSL) work?

SSL encrypts data transmitted between a client and server to ensure confidentiality and integrity. This process involves a handshake for authentication and key exchange, followed by data encryption using symmetric encryption algorithms. SSL also ensures data integrity through cryptographic hash functions and session termination.

### 53. What do you mean by the Security Information and Event Management (SIEM) System? 

A Security Information and Event Management (SIEM) system is a centralized platform that collects, aggregates, and analyzes security-related data from various sources within an organization's IT infrastructure. 

### 54. What are APT Threats? 

Advanced Persistent Threats (APTs) are targeted cyberattacks orchestrated by highly skilled and well-funded adversaries, such as nation-states or organized cybercriminal groups. APT actors employ various tactics, techniques, and procedures (TTPs) to access the victim's infrastructure and steal sensitive data. 

### 55. What are the challenges in the Security of Wireless Networks? 

Unlike wired networks, where data travels through physical cables and is relatively contained within the confines of a building or premises, wireless networks transmit data through radio waves, which can extend beyond the physical boundaries of an organization's premises. 

Hence, we face the following challenges: 

- Unauthorized access points set up by employees or attackers can create vulnerabilities in the network.
- Wireless signals can be intercepted by attackers to capture sensitive information such as passwords or financial data.
- Ensuring that only authorized users can access the network, and enforcing proper authentication and authorization protocols can be challenging in wireless environments.

### 56. What is BYOD in Cyber Security? 

BYOD stands for the Bring Your Own Device. It is the challenge that organizations face in cyber security systems. In this challenge, when the personal devices are connected to the corporate networks, security risks arise. This is because these devices may not adhere to the same security standards as company-owned devices. 

### 57. What is EDR in Cyber Security? 

Endpoint Detection and Response (EDR) solutions are critical components of modern cybersecurity strategies. They focus on detecting and responding to threats targeting endpoint devices such as laptops, desktops, servers, and mobile devices. They generate the alert so that the security teams can prioritize and respond to genuine threats effectively.## Cyber Security Interview Questions for Freshers

### 1. Define Cybersecurity?

In general, we can say that Cyber Security deals with protecting digital systems, networks, and data from unauthorized access, cyberattacks, and malicious activities. The main goal of cybersecurity is to safeguard the system from various threats, including viruses, malware, ransomware, phishing, and insider threats. To achieve this goal, it implements practices like encryption, firewalls, intrusion detection systems (IDS), vulnerability assessments, and security awareness training. 

|   |
|---|
|**Gain essential skills to defend your organization from security threats by enrolling in our [Cyber Security Training](https://mindmajix.com/cyber-security-training "Cyber Security Training").**|

### 2. What is Cryptography?

Cryptography is a method to transform and transmit confidential data in an encoded way to protect the information from third parties for whom data is not authorized. It involves the transformation of plaintext (unencrypted data) into ciphertext (encrypted data) using mathematical algorithms and cryptographic techniques.

### 3. How does the Encryption Work? 

Encryption works by converting plaintext data into ciphertext using encryption algorithms and keys. The encryption process scrambles the original data which makes it unreadable to unauthorized users. To decrypt the ciphertext and retrieve the original data, the recipient uses a decryption key. Hence, the data can be communicated between the systems confidentially. 

### 4. What is the difference between Threat, Vulnerability, and Risk?

**Threat:** It is the factor with the potential to cause harm by damaging or destroying the official data of a system or organization. For example, a Distributed Denial of Service (DDoS) attack is a threat where attackers flood a network or server with excessive traffic, causing it to become unavailable to legitimate users.

**Vulnerability:** It refers to weaknesses in a system that makes threat outcomes more possible and even more dangerous. An example of a vulnerability is outdated software that hasn't been patched against known security vulnerabilities.

**Risk:** It refers to a combination of threat probability and impact/loss. In simple terms, it is related to potential damage or loss when a threat exploits the vulnerability. The Risk is calculated using the Threat probability and Potential loss. 

_Risk = Threat probability * Potential loss_ 

### 

### 5. What are the latest tools and frameworks for Cyber Security?

Below are the top tools along with later versions that you must be aware about during your Cyber Security Interview. 

- **Metasploit:** It is the penetration testing framework for finding and exploiting vulnerabilities in systems. Its latest version for the Metasploit Pro is 4.22.2. 
- **John the Ripper:**  This is a password-cracking tool used to detect weak passwords and hash encryption. Its latest jumbo version is 1.9.0.
- **Wireshark:** it is the network protocol analyzer that captures and inspects data packets on a network. Its latest stable release is 4.2.4.  
- **NetStumbler:** It comes as the wireless network scanner for Windows systems with the latest version 0.4.0. 
- **Forcepoint:** It is a renowned cybersecurity company offering solutions for data protection and threat intelligence.
- **Aircrack-ng:** This is the complete suite of wireless network security tools for assessing Wi-Fi security. Its latest version is 1.7. 

### 6. What is the difference between IDS and IPS?

|   |   |
|---|---|
|**Intrusion Detection Systems (IDS)**|**Intrusion Prevention Systems (IPS)**|
|It only detects intrusions but is unable to prevent intrusions.|It detects and prevents intrusions.|
|It's a monitoring system.|It’s a control system.|
|It needs a human or another system to look at the results.|It needs a regularly updated database with the latest threat data.|

### 7. What is a Botnet?

 A Botnet is a group of internet-connected devices such as servers, PCs, mobile devices, etc., that are affected and controlled by malware.

It is used for stealing data, sending spam, performing distributed denial-of-service attack (DDoS attack), and more, and also to enable the user to access the device and its connection.

### 8. What is a CIA triad?

 CIA (confidentiality, integrity, and availability) triad is a model designed to handle policies for information security within an organization.

- **Confidentiality -** A collection of rules that limits access to information.
- **Integrity -** It assures the information is trustworthy and reliable.
- **Availability -** It provides reliable access to data for authorized people.

### 9. Symmetric Vs Asymmetric encryption.

|   |   |   |
|---|---|---|
|**Purpose**|**Symmetric Encryption**|**Asymmetric Encryption**|
|**Encryption:**|Uses a single key to encrypt and decrypt information.|Uses a pair of public and private keys to encrypt and decrypt information.|
|**Speed:**|Symmetric encryption performs faster|Asymmetric encryption performs slower compared to symmetric encryption.|
|**Algorithms:**|AES, RC4, DES, QUAD, 3DES, Blowfish, etc.|Diffie-Hellman and RSA|
|**Purpose:**|Preferred for transferring huge data|Mostly used for exchanging secret keys safely.|

### 10. What is the difference between hashing and encryption?

 Both hashing and encryption are used to convert readable data into an unreadable format. The significant difference is that encrypted data can be transformed into original data by decryption, whereas hashed data cannot be processed back to the original data.

### 11. What is two-factor authentication and how it can be implemented for public websites?

- Tw0-factor authentication is also referred to as dual-factor authentication or two-step verification where the user provides two authentication factors for protecting both user credentials and resources while accessing. 
- The two-factor authentication can be implemented on public websites such as Twitter, Microsoft, LinkedIn, and more for enabling another protection on your already protected account with a password.
- For enabling this double factor authentication, you can easily go to settings and then manage security settings.

|   |
|---|
|**Related Article: [Cyber Security Frameworks](https://mindmajix.com/cyber-security-frameworks "Cyber Security Frameworks")**|

### 12. What is the use of a firewall and how it can be implemented?

 A firewall is a security system used to control and monitor network traffic. It is used for protecting the system/network from malware, viruses, worms, etc., and secures unauthorized access from a private network.

The steps required to set up and configure the firewall are listed below: 

- Change the default password for a firewall device.
- Disable the remote administration feature.
- Configure port forwarding for specific applications to function correctly, such as an FTP server or a web server.
- Firewall installation on a network with an existing DHCP server can cause errors unless its firewall’s DHCP is disabled. 
- Make sure the firewall is configured to robust security policies.

[![MindMajix YouTube Channel](https://mindmajix.com/_next/image?url=https%3A%2F%2Fcdn.mindmajix.com%2Fblog%2Fimages%2Fyoutube-banner-ultimate-version.png&w=1920&q=75)](https://bit.ly/3if9dmk "Subscribe MindMajix YouTube Channel")

### 13. What is the difference between vulnerability assessment and penetration testing?

- The terms Vulnerability assessment and penetration testing are both different, but serve an essential function of protecting the network environment.
- Vulnerability Assessment: It’s a process to define, detect, and prioritize the vulnerabilities in computer systems, network infrastructure, applications, etc., and gives the organization the required information to fix the flaws. 
- Penetration Testing: It is also called pen testing or ethical hacking. It’s a process of testing a network, system, application, etc. to identify vulnerabilities that attackers could exploit. In the context of web application security, it is most widely used to augment a web application firewall (WAF).

### 14. What is the difference between stored and reflected XSS?

- **Stored XSS Attacks -** The attacks where the injected scripts are stored on the target servers permanently. In this, the victim retrieves the malicious script from the server when requests the stored information.
- **Reflected XSS Attacks -** In this, the user has to send the request first, then it will start running on the victim’s browser and reflects results from the browser to the user who sent the request.

### 15. What is a three-way handshake process?

A three-way handshake process is used in TCP (Transmission Control Protocol) network for the transmission of data in a reliable way between the host and the client.

It’s called a three-way handshake because three segments are exchanged between the server and the client. 

- **SYN:** The client wants to establish a connection with the server, and sends a segment with SYN(Synchronize Sequence Number) to the server if the server is up and has open ports.
- **SYN + ACK:** The server responds to the client request with SYN-ACK signal bits set if it has open ports.
- **ACK:** The client acknowledges the response of a server and sends an ACK(Acknowledgment) packet back to the server.

|   |
|---|
|**Learn [Cyber Security Training in Bangalore](https://mindmajix.com/cyber-security-training-bangalore "Cyber Security Training in Bangalore")**|

### 16. What are the techniques used in preventing a Brute Force Attack?

A brute Force Attack is a trial and error method that is employed for application programs to decode encrypted data such as data encryption keys or passwords using brute force rather than intellectual strategies. It’s a way to identify the right credentials by repetitively attempting all the possible methods.

Brute Force attacks can be avoided by the following practices:

- Adding password complexity: Include different formats of characters to make passwords stronger.
- Limit login attempts: set a limit on login failures.
- Two-factor authentication: Add this layer of security to avoid brute-force attacks.

## Cyber Security Interview Questions for Experienced

### 17. List the common types of cybersecurity attacks.

The following are the most common types of cybersecurity attacks:

- Denial-of-Service (DoS): Overloading websites or networks to make them crash and stop working.
- Man-in-the-Middle Attacks: Secretly listening in on conversations between people or computers to steal information.
- Credential Reuse: Using the same usernames and passwords across different accounts to break into them.
- Phishing: Tricking people into giving away their personal info, like passwords or credit card numbers, through fake emails or websites.
- Session Hijacking: Taking control of someone's online session to pretend to be them and access their stuff.
- Malware: Bad software that harms your computer or steals your information.
- SQL Injection Attack: Tricking websites to do things they shouldn't, like messing with their databases.
- Cross-site scripting (XSS): Sneaking bad code into websites to steal info from users or make them do things they don't want to.

### 18 Define data leakage and its types.

Data Leakage refers to the illegal transmission of data to an external destination or unauthorized entity within an organization. It can transfer data either physically or electronically. It usually occurs via the web, emails, and mobile data storage devices.

Types of data leakage:

1. **The Accidental Breach -** The majority of data leakage incidents are accidental.
2.  **Ex:** An entity may choose the wrong recipient while sending confidential data.
3. **The Disgruntled or ill-intentioned Employee -** The authorized entity sends confidential data to an unauthorized body. 
4. **Electronic Communications with Malicious Intent -** The problem is all electronic mediums are capable of file transferring and external access sources over the internet.

### 19. What is the use of a Traceroute?

A Traceroute is a network diagnostic tool, used for tracking the pathway of an IP network from source to destination. It records the period of each hop the packet makes while its route to its destination.

### 20. How to prevent CSRF attacks?

CSRF is referred to as Cross-site Request Forgery, where an attacker tricks a victim into performing actions on their behalf.

CSRF attacks can be prevented by using the following ways:

- Employing the latest antivirus software which helps in blocking malicious scripts.
- While authenticating to your banking site or performing any financial transactions on any other website do not browse other sites or open any emails, which helps in executing malicious scripts while being authenticated to a financial site.
- Never save your login/password within your browser for financial transactions.
- Disable scripting in your browser.

|   |
|---|
|**Related Article: [Cyber Attacks and Preventions Methods](https://mindmajix.com/cyber-security-interview-questions "Cyber Attacks and Preventions Methods")**|

### 21. What is port scanning?

A port scanning is an application designed for identifying open ports and services accessible on a host network. Security administrators mostly utilize it for exploiting vulnerabilities, and also by hackers for targeting victims.

Some of the most popular port scanning techniques are listed below:

- Ping scan
- TCP connect
- TCP half-open
- Stealth scanning – NULL, FIN, X-MAS
- UDP

### 22. What is the need for DNS monitoring?

- DNS (Domain Name System) is a service that is used for converting user-friendly domain names into a computer-friendly IP address. It allows websites under a particular domain name that is easy to remember.
- DNS monitoring is nothing but monitoring DNS records to ensure does it route traffic properly to your website, electronic communication, services, and more.

### 23. What is the difference between hashing and salting?

- Hashing is majorly used for authentication and is a one-way function where data is planned to a fixed-length value.
- Salting is an extra step for hashing, where it adds additional value to passwords that change the hash value created.

### 24. How to prevent a ‘Man-in-the-Middle Attack’?

The following practices prevent the ‘Man-in-the-Middle Attacks’:

- Have stronger WAP/WEP Encryption on wireless access points avoids unauthorized users.
- Use a VPN for a secure environment to protect sensitive information. It uses key-based encryption.
- Public key pair-based authentication must be used in various layers of a stack for ensuring whether you are communicating the right things are not.
- HTTPS must be employed for securely communicating over HTTP through the public-private key exchange.

### 25. What are the common methods of authentication for network security? 

- **Biometrics -** It is a known and registered physical attribute of a user specifically used for verifying their identity. 
- **Token -** A token is used for accessing systems. It makes it more difficult for hackers to access accounts as they have long credentials.
- **Transaction Authentication -** A one-time pin or password is used in processing online transactions through which they verify their identity.
- **Multi-Factor Authentication -**  It’s a security system that needs more than one method of authentication.
- **Out-of-Band Authentication -** This authentication needs two different signals from two different channels or networks. It prevents most of the attacks from hacking and identity thefts in online banking.

|   |
|---|
|**Related Article: [Cyber Security Career Path](https://mindmajix.com/cyber-security-career-path "Cyber Security Career Path")**|

### 26. Which is more secure SSL or HTTPS?

- SSL (Secure Sockets Layer) is a secure protocol that provides safer conversations between two or more parties across the internet. It works on top of the HTTP to provide security.
- HTTPS (Hypertext Transfer Protocol Secure) is a combination of HTTP and SSL to provide a safer browsing experience with encryption.
- In terms of security, SSL is more secure than HTTPS.

### 27. What is the difference between black hat, white hat, and grey hat hackers? 

- A black-hat hacker is a person who tries to obtain unauthorized access into a system or a network to steal information for malicious purposes.
- White-hat hackers are also known as ethical hackers; they are well-versed with ethical hacking tools, methodologies, and tactics for securing organization data. They try to detect and fix vulnerabilities and security holes in the systems. Many top companies recruit white hat hackers.
- A grey hat hacker is a computer security expert who may violate ethical standards or rules sometimes but does not have the malicious intent of a black hat hacker.

### 28. What is cognitive security?

Cognitive security is one of the applications of AI technologies that is used explicitly for identifying threats and protecting physical and digital systems based on human understanding processes.

Self-learning security systems use pattern recognition, natural language processing, and data mining to mimic the human brain.

### 

### 29. What is phishing and how it can be prevented?

Phishing is a malicious attempt of pretending oneself as an authorized entity in electronic communication for obtaining sensitive information such as usernames, passwords, etc. through fraudulent messages and emails.

The following practices can prevent phishing:

- Use firewalls on your networks and systems.
- Enable robust antivirus protection that has internet security.
- Use two-factor authentication wherever possible
- Maintain adequate security.
- Don't enter sensitive information such as financial or digital transaction details on web pages that you don't trust.
- Keep yourself updated with the latest phishing attempts.

### 30. What is SQL injection and how it can be prevented?

SQL Injection (SQLi) is a type of code injection attack where it manages to execute malicious SQL statements to control a database server behind a web application. Attackers mostly use this to avoid application security measures and thereby access, modify, and delete unauthorized data.

The following ways will help you to mitigate or prevent SQL injection attacks:

- Include Prepared Statements (with Parameterized Queries)
- Use Stored Procedures
- Validate user input
- Hide data from the error message
- Update your system
- Store database credentials separate and encrypted
- Disable shell and any other functionalities you don’t need

|   |
|---|
|**Visit here to learn [Cyber Security Training in Hyderabad](https://mindmajix.com/cyber-security-training-hyderabad "Cyber Security Training Hyderabad")**|

### 31. How will you keep yourself updated with the latest cybersecurity news?

The following ways will help you to keep up with the latest cybersecurity updates:

- Follow news websites and blogs from security experts. 
- Browse security-related social media topics.
- Check vulnerability alert feeds and advisory sites.
- Attend cybersecurity live events.

### 32. What is a DDOS attack and how to stop and prevent them?

A DDOS (distributed denial-of-service ) is a malicious attempt of disrupting regular traffic of a network by flooding with a large number of requests and making the server unavailable to the appropriate requests. The requests come from several unauthorized sources and hence called distributed denial of service attacks.

The following methods will help you to stop and prevent DDOS attacks:

- Build a denial of service response plan
- Protect your network infrastructure
- Employ basic network security
- Maintain strong network architecture
- Understand the Warning Signs
- Consider DDoS as a service

### 33. What is Cross-Site Scripting and how it can be prevented?

Cross-site scripting is also known as a client-side injection attack, which aims at executing malicious scripts on a victim’s web browser by injecting malicious code.

- The following practices can prevent Cross-Site Scripting:
- Encoding special characters
- Using XSS HTML Filter
- Validating user inputs
- Using Anti-XSS services/tools

## Frequently Asked Cyber Security Interview Questions 

### 33. What do you understand by compliance in Cybersecurity?

- Compliance means living by a set of standards set by an organization/government/independent party. 
- It helps in defining and achieving IT targets and also in mitigating threats through processes like vulnerability management.

### 34. What is the use of Patch Management?

- The purpose of patch management is to keep updating various systems in a network and protect them against malware and hacking attacks.
- Many enterprise patch management tools manage the patching process by installing or deploying agents on a target computer, and they provide a link between centralized patch servers and computers to be patched.

### 35. What is the difference between a false positive and a false negative in IDS?

- A false positive is considered to be a false alarm and a false negative is considered to be the most complicated state.
- A false positive occurs when an IDS fires an alarm for legitimate network activity.
- A false negative occurs when IDS fails to identify malicious network traffic.

Compared to both, a false positive is more acceptable than a false negative as they lead to intrusions without getting noticed.

|   |
|---|
|**Related Article: [Top 10 Cybersecurity Tools In 2020](https://mindmajix.com/cybersecurity-tools "Top 10 Cybersecurity Tools In 2020")**|

### 36 what is the difference between the Red Team and the Blue team?

- The red team and blue team refer to cyberwarfare. Many organizations split the security team into two groups as red team and blue team.
- The red team refers to an attacker who exploits weaknesses in an organization's security.
- The blue team refers to a defender who identifies and patches vulnerabilities into successful breaches.

### 37. Explain System hardening?

- Generally, system hardening refers to a combination of tools and techniques for controlling vulnerabilities in systems, applications, firmware, and more in an organization. 
- The purpose of system hardening is to decrease the security risks by reducing the potential attacks and condensing the system’s attack surface.

The following are the various types of system hardening:

1. Database hardening
2. Operating system hardening
3. Application hardening
4. Server hardening
5. Network hardening

### 38. What is a cybersecurity risk assessment?

A cybersecurity risk assessment refers to detecting the information assets that are prone to cyber-attacks(including customer data, hardware, laptop, etc.) and also evaluates various risks that could affect those assets.

It is mostly performed to identify, evaluate, and prioritize risks across organizations.

The best way to perform cybersecurity risk assessment is to detect:

- Relevant threats in your organization 
- Internal and external vulnerabilities 
- Evaluate vulnerabilities impact if they are exploited

### 39. What are the seven layers of the OSI model?

The main objective of the OSI model is to process the communication between two endpoints in a network.

The seven open systems interconnection layers are listed below:

- **Application layer (layer 7) -** It allows users to communicate with network/application whenever required to perform network-related operations. 
- **Presentation layer (layer 6) -** It manages encryption and decryption of data required for the application layer. It translates or formats data for the application layer based on the syntax of the application that accepts.
- **Session layer (layer 5) -** It determines the period of a system that waits for other applications to respond.
- **Transport layer (layer 4) -** It is used for sending data across a network and also offers error checking practices and data flow controls.
- **Network layer (layer 3) -** It is used to transfer data to and fro through another network.
- **Data-link layer (layer 2) -** It handles the flow of data to and fro in a network. It also controls problems that occur due to bit transmission errors.
- **Physical layer (layer 1) -** It transfers the computer bits from one device to another through the network. It also controls how physical connections are set up to the network and also bits represented into signals while transmitting either optically, electrically, or radio waves.

### 40. How to reset or remove the BIOS password?

There are many ways to reset or remove the BIOS password:

- By removing the CMOS battery
- By using software
- By using the MS-DOS command
- By using motherboard jumper
- By using Backdoor BIOS password

|   |
|---|
|**Related Article: [How to Become a Cyber Security Engineer](https://mindmajix.com/how-to-become-a-cyber-security-engineer "How to Become a Cyber Security Engineer")**|

### 41. What is the use of Address Resolution Protocol (ARP)?

ARP is a protocol specifically used to map IP network addresses to physical addresses, such as Ethernet addresses.

It translates 32-bits addresses to 48-bits addresses and vice versa. This is needed because the most common level of internet protocol(IP) we use today is 32-bits long and MAC addresses are 48-bits long.

### 42. How to protect data in transit Vs rest?

|   |   |   |
|---|---|---|
|**Description**|**Data in Transit**|**Data in Rest**|
|Definition of data|Here data moves actively from one location to another across the internet or private network.|Here data is not transferred from one location to another as data is stored on hard drives, flash drives, etc.|
|Encryption in data protection|It encrypts sensitive data before sending or using encrypted connections(SSL, HTTPS, TLS, etc.)|It encrypts sensitive files before storing or choosing the encrypted storage drive itself.|

### 43. What are the several indicators of compromise(IOC) that organizations should monitor?

The key indicators of compromise that organizations should monitor are listed below:

- Unusual Outbound Network Traffic
- HTML Response Sizes
- Geographical Irregularities
- Increases in Database Read Volume
- Log-In Red Flags
- Unexpected Patching of Systems
- Large Numbers of Requests for the Same File
- Web Traffic with Unhuman Behavior
- Suspicious Registry or System File Changes
- Unusual DNS Requests
- Mobile Device Profile Changes
- Bundles of Data in the Wrong Place
- Mismatched Port-Application Traffic
- Signs of DDoS Activity
- Anomalies in Privileged User Account Activity

### 44. What is Remote Desktop Protocol (RDP)?

- RDP (Remote Desktop Protocol) is a Microsoft protocol specifically designed for application data transfer security and encryption between client devices, users, and a virtual network server.
- It allows administrators to remotely evaluate and resolve issues individual subscribers encounter.
- It supports up to 64,000 separate data channels with a provision for multipoint transmission.

### 45. What is the difference between Diffie Hellman and RSA? 

- **Diffie-Helman:** It’s a key exchange protocol where two parties exchange a shared key that either one can use to encrypt/decrypt messages between them.
- **RSA:** It’s asymmetric key encryption where it has two different keys. The public key can be given to anyone and decrypted with another, which is kept private.

|   |
|---|
|**Related Article: [Cyber Security Best Practices](https://mindmajix.com/top-10-cybersecurity-best-practices "Cyber Security Best Practices")**|

### 46. What is Forward Secrecy and how does it work? 

- Forward secrecy is a feature of specific key agreement protocols which gives assurance that even if the private key of the server is compromised the session keys will not be compromised. It is also known as perfect forward secrecy(PFS).
- The Algorithm that helps in achieving this is called "Diffie–Hellman key exchange".

### 47. What is an active reconnaissance? 

- Active reconnaissance is a kind of computer attack where an intruder engages the target system for collecting data about vulnerabilities.
- The attackers mostly use port scanning to identify vulnerable ports and then exploit the vulnerabilities of services that are associated with open ports.

|   |
|---|
|**Leave an Inquiry to learn [Cyber Security Training in Houston](https://mindmajix.com/cyber-security-training-houston)**|

### 48. What is security misconfiguration?

Security misconfiguration is a vulnerability that could happen if an application/network/device is susceptible to attack due to an insecure configuration option. It can be as simple as keeping the default username/password unchanged.

### 49. What is the difference between information protection and information assurance?

- **Information protection:** It protects the data using encryption, security software, etc., from unauthorized access.
- **Information Assurance:** It keeps the data reliable by ensuring availability, authentication, confidentiality, etc.

### 50. What do you mean by Chain of Custody?

- Chain of custody refers to the probability of data provided as originally acquired and has not been changed before admission into evidence.
- In legal terms, it’s a chronological documentation/paper trail that records a proper sequence of custody, control, analysis, and disposition of electronic or physical evidence.

### 51. What is a zero-day vulnerability? 

A zero-day vulnerability is a software security flaw that is unknown to the vendor or developer and has not yet been patched or fixed. Attackers use these vulnerabilities before the software's developer becomes aware of them. That is why it is called "zero-day," as there are zero days of advance notice to avoid the risk.

### 52. How does a Secure Socket Layer (SSL) work?

SSL encrypts data transmitted between a client and server to ensure confidentiality and integrity. This process involves a handshake for authentication and key exchange, followed by data encryption using symmetric encryption algorithms. SSL also ensures data integrity through cryptographic hash functions and session termination.

### 53. What do you mean by the Security Information and Event Management (SIEM) System? 

A Security Information and Event Management (SIEM) system is a centralized platform that collects, aggregates, and analyzes security-related data from various sources within an organization's IT infrastructure. 

### 54. What are APT Threats? 

Advanced Persistent Threats (APTs) are targeted cyberattacks orchestrated by highly skilled and well-funded adversaries, such as nation-states or organized cybercriminal groups. APT actors employ various tactics, techniques, and procedures (TTPs) to access the victim's infrastructure and steal sensitive data. 

### 55. What are the challenges in the Security of Wireless Networks? 

Unlike wired networks, where data travels through physical cables and is relatively contained within the confines of a building or premises, wireless networks transmit data through radio waves, which can extend beyond the physical boundaries of an organization's premises. 

Hence, we face the following challenges: 

- Unauthorized access points set up by employees or attackers can create vulnerabilities in the network.
- Wireless signals can be intercepted by attackers to capture sensitive information such as passwords or financial data.
- Ensuring that only authorized users can access the network, and enforcing proper authentication and authorization protocols can be challenging in wireless environments.

### 56. What is BYOD in Cyber Security? 

BYOD stands for the Bring Your Own Device. It is the challenge that organizations face in cyber security systems. In this challenge, when the personal devices are connected to the corporate networks, security risks arise. This is because these devices may not adhere to the same security standards as company-owned devices. 

### 57. What is EDR in Cyber Security? 

Endpoint Detection and Response (EDR) solutions are critical components of modern cybersecurity strategies. They focus on detecting and responding to threats targeting endpoint devices such as laptops, desktops, servers, and mobile devices. They generate the alert so that the security teams can prioritize and respond to genuine threats effectively.

‍