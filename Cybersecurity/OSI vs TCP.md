The **OSI model** (Open Systems Interconnection) and the **TCP/IP model** (Transmission Control Protocol/Internet Protocol) are both conceptual frameworks used to understand and design network communication. They describe how data is transmitted over a network and help standardize communication between devices. Let’s compare them and break them down in an easy-to-understand way.

---

### **OSI Model (7 Layers)**

The **OSI model** divides the communication process into 7 distinct layers, each responsible for a specific part of the communication. Think of it like building a house: each layer adds another "floor" to the house.

1. **Layer 7: Application Layer**
    
    - **What it does**: This layer is the closest to the user and provides services like web browsing, email, file transfers, etc.
    - **Example**: When you use a web browser (HTTP) or send an email (SMTP), you are using the application layer.
2. **Layer 6: Presentation Layer**
    
    - **What it does**: Translates or formats data for the application layer. It ensures that data is in the correct format for the recipient, handling encryption, compression, and encoding.
    - **Example**: JPEG for images, MP3 for audio, or encryption protocols like SSL/TLS.
3. **Layer 5: Session Layer**
    
    - **What it does**: Manages communication sessions between applications on different devices, controlling the start, duration, and termination of communication.
    - **Example**: Keeping a session active when you're logged into a website, or managing a video call.
4. **Layer 4: Transport Layer**
    
    - **What it does**: Ensures that data is transferred reliably between devices, and manages error recovery, flow control, and retransmissions if needed.
    - **Protocols**: **TCP** (connection-oriented, reliable), **UDP** (connectionless, faster but less reliable).
    - **Example**: Downloading a file over the internet uses **TCP** to ensure the file arrives correctly.
5. **Layer 3: Network Layer**
    
    - **What it does**: Determines the best path for data to travel through the network, and handles logical addressing (like IP addresses).
    - **Protocols**: **IP** (Internet Protocol), **ICMP** (used for network diagnostics like ping).
    - **Example**: When data is sent from one computer to another over the internet, IP handles routing it through different networks.
6. **Layer 2: Data Link Layer**
    
    - **What it does**: Transfers data between adjacent network nodes and handles **MAC addresses** (Media Access Control), ensuring that data frames are error-free as they travel across a local network.
    - **Example**: Ethernet, Wi-Fi. Your device uses this layer to send data to a router or switch over a local area network (LAN).
7. **Layer 1: Physical Layer**
    
    - **What it does**: Transmits raw bitstreams (1s and 0s) over the physical medium like cables, fiber optics, or radio waves.
    - **Example**: Network cables, hubs, switches, and physical connections like Wi-Fi signals.

---

### **TCP/IP Model (4 Layers)**

The **TCP/IP model** is a simpler, more practical model used to describe internet communication. It has 4 layers and is the basis for the modern internet.

1. **Application Layer**
    
    - **What it does**: Combines the functions of the OSI Application, Presentation, and Session layers. This layer handles high-level protocols like HTTP, FTP, DNS, and more.
    - **Example**: Your browser accessing a website or sending an email.
2. **Transport Layer**
    
    - **What it does**: Responsible for communication between devices, ensuring reliable data transmission, flow control, and error checking (like in the OSI model).
    - **Protocols**: **TCP** (reliable, connection-oriented), **UDP** (faster but unreliable).
    - **Example**: Streaming a video using UDP or downloading a file using TCP.
3. **Internet Layer**
    
    - **What it does**: Equivalent to the Network Layer in OSI. It deals with logical addressing (IP addresses) and routing data across different networks.
    - **Protocols**: **IP**, **ICMP** (for error messages and diagnostics).
    - **Example**: Routing data packets between devices on different networks using IP addresses.
4. **Network Interface (Link) Layer**
    
    - **What it does**: Combines the OSI Data Link and Physical layers. This layer handles how data is physically sent across the network and how devices are addressed at the hardware level.
    - **Example**: Ethernet, Wi-Fi, and ARP (Address Resolution Protocol) which translates IP addresses to MAC addresses for local delivery.

---

### **Comparison: OSI vs. TCP/IP**

|**Aspect**|**OSI Model**|**TCP/IP Model**|
|---|---|---|
|**Layers**|7 Layers|4 Layers|
|**Development**|Developed by ISO|Developed by DoD/ARPA|
|**Conceptual/Practical**|Mostly a conceptual model|Practical and used in real life|
|**Application Layer**|Divided into 3 layers (Application, Presentation, Session)|All handled by the Application Layer|
|**Transport Layer**|Includes TCP, UDP, flow control, error correction|Similar to OSI, includes TCP, UDP|
|**Internet Layer (Network)**|Handles IP routing, logical addressing|Handles IP routing, logical addressing|
|**Network Interface (Link)**|Divided into Data Link and Physical layers|Combines Data Link and Physical into one|

---

### **Examples for each layer**

- **OSI Layer 1 (Physical)**: A network cable or Wi-Fi signal.
- **OSI Layer 2 (Data Link)**: A switch directing Ethernet frames by their MAC addresses.
- **OSI Layer 3 (Network)**: A router forwarding packets based on IP addresses.
- **OSI Layer 4 (Transport)**: TCP ensuring that all parts of a file download arrive intact.
- **OSI Layer 5 (Session)**: Maintaining a VPN connection session.
- **OSI Layer 6 (Presentation)**: Encrypting a message using SSL/TLS (HTTPS).
- **OSI Layer 7 (Application)**: A web browser using HTTP to load a website.

For the **TCP/IP model**, the layers map roughly to these OSI layers:

- **Network Interface** = OSI Layers 1 and 2
- **Internet Layer** = OSI Layer 3
- **Transport Layer** = OSI Layer 4
- **Application Layer** = OSI Layers 5, 6, and 7.

---

### Key Takeaways:

- The **OSI model** is more of a **theoretical framework** with 7 layers, while the **TCP/IP model** is a **practical framework** that is used for internet communication.
- **TCP/IP** is simpler and directly maps to real-world internet protocols like HTTP, TCP, and IP.





### The Life of a Packet

Based on what we have studied so far, we can explain a _simplified version_ of the packet’s life. Let’s consider the scenario where you search for a room on TryHackMe.

1. On the TryHackMe search page, you enter your search query and hit enter.
2. Your web browser, using HTTPS, prepares an HTTP request and pushes it to the layer below it, the transport layer.
3. The TCP layer needs to establish a connection via a three-way handshake between your browser and the TryHackMe web server. After establishing the TCP connection, it can send the HTTP request containing the search query. Each TCP segment created is sent to the layer below it, the Internet layer.
4. The IP layer adds the source IP address, i.e., your computer, and the destination IP address, i.e., the IP address of the TryHackMe web server. For this packet to reach the router, your laptop delivers it to the layer below it, the link layer.
5. Depending on the protocol, The link layer adds the proper link layer header and trailer, and the packet is sent to the router.
6. The router removes the link layer header and trailer, inspects the IP destination, among other fields, and routes the packet to the proper link. Each router repeats this process until it reaches the router of the target server.

The steps will then be reversed as the packet reaches the router of the destination network. As we cover additional protocols, we will revisit this exercise and create a more in-depth version.