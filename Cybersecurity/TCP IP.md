**Transmission Control Protocol (TCP)** is one of the core protocols of the internet's transport layer. It is a **connection-oriented protocol** that provides reliable communication between two hosts over an IP network. TCP ensures that data sent from one host is delivered to the other host in the correct order and without any loss, duplication, or corruption.

Here's a deeper explanation of the TCP protocol and its key features:

### **Key Features of TCP**

1. **Connection-Oriented Protocol**:
    
    - Before any data can be exchanged between two devices, TCP establishes a connection using a process called the **three-way handshake**. This ensures both sides are ready for communication and establishes a reliable connection.
2. **Reliable Delivery**:
    
    - TCP guarantees that the data being transmitted will reach its destination in the correct order and without errors. If packets are lost or damaged in transit, TCP will automatically detect the issue and retransmit the packets.
3. **Flow Control**:
    
    - TCP uses flow control to prevent a sender from overwhelming a receiver with too much data too quickly. It uses a mechanism called the **sliding window** to regulate the amount of data being sent.
4. **Congestion Control**:
    
    - TCP monitors the network for congestion and adjusts the rate at which it sends data to avoid network overload. This is critical for maintaining network stability.
5. **Segmentation and Reassembly**:
    
    - TCP breaks data into smaller packets called **segments**. Each segment is sent individually, and the receiver reassembles these segments back into the original data stream.
6. **Error Detection and Recovery**:
    
    - TCP uses **checksums** to detect errors in transmitted data. If errors are detected, TCP ensures that the corrupted data is retransmitted.


### What is Three-Way Handshake?

![enter image description here](https://cdn.prod.website-files.com/647e4e328280afb2dff45d0e/65f9f2db63c58ae0b5e9a874_68747470733a2f2f756d7574746f73756e2e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031392f30392f39345f73796e5f666967315f6c672e6a7067.jpeg)

TCP uses a three-way handshake to establish a reliable connection. The connection is full duplex, and both sides synchronize (SYN) and acknowledge (ACK) each other.

The client chooses an initial sequence number, set in the first SYN packet. The server also chooses its own initial sequence number, set in the SYN/ACK packet.

Each side acknowledges each other's sequence number by incrementing it; this is the acknowledgement number. The use of sequence and acknowledgment numbers allows both sides to detect missing or out-of-order segments.

Once a connection is established, ACKs typically follow for each segment. The connection will eventually end with a RST (reset or tear down the connection) or FIN (gracefully end the connection). ([ScienceDirect](https://www.sciencedirect.com/topics/computer-science/three-way-handshake))

### **TCP Segment Structure**

Each TCP segment has a specific structure that contains important information for managing the connection. Some key fields in a TCP segment are:

1. **Source Port** and **Destination Port**:  
    These specify the port numbers used by the sending and receiving applications.
    
2. **Sequence Number**:  
    This is a unique number assigned to each byte of data, ensuring that the receiver can reassemble the data in the correct order.
    
3. **Acknowledgment Number**:  
    This indicates the next expected byte from the sender. It’s used to acknowledge receipt of data.
    
4. **Data Offset**:  
    Specifies where the data begins in the segment.
    
5. **Flags**:  
    TCP has several flags that control the flow of data. Common ones include:
    
    - **SYN**: Used during connection establishment.
    - **ACK**: Acknowledges received data.
    - **FIN**: Used to close a connection.
    - **RST**: Resets a connection in case of errors.
    - **PSH**: Pushes data immediately to the receiving application.
    - **URG**: Urgent data.
6. **Window Size**:  
    Controls the flow of data by indicating how much data the receiver is willing to accept at one time.
    
7. **Checksum**:  
    Used to detect errors in the segment. If the checksum does not match, the segment is discarded, and the sender will retransmit it.
### **The Three-Way Handshake (Connection Establishment)**

Before two devices can communicate, they use a **three-way handshake** to establish a connection:

1. **SYN (Synchronize)**:  
    The client sends a **SYN** packet to the server to request a connection. This packet contains an initial sequence number (ISN) for the connection.
    
2. **SYN-ACK**:  
    The server responds with a **SYN-ACK** packet, acknowledging the client’s request and providing its own sequence number.
    
3. **ACK**:  
    The client sends an **ACK** packet to acknowledge the server’s sequence number, completing the handshake.
    

After this handshake, both the client and server are ready to exchange data.

### **Data Transmission and Flow Control**

- Once the connection is established, TCP begins transmitting data in segments. As each segment is received, the receiver acknowledges it by sending an **ACK** message that includes the next expected sequence number.
    
- TCP uses **flow control** to ensure that neither side sends more data than the other can handle. This is done using the **window size** field. The sender can only send data up to the window size specified by the receiver. If the receiver’s buffer is full, it will reduce the window size, telling the sender to slow down.
### **TCP vs. UDP**

It’s also helpful to understand how TCP differs from **UDP (User Datagram Protocol)**:

|Feature|TCP|UDP|
|---|---|---|
|**Connection**|Connection-oriented (requires handshake)|Connectionless (no handshake)|
|**Reliability**|Reliable (data is retransmitted if lost)|Unreliable (no retransmission)|
|**Order**|Data is delivered in the correct order|No guarantee of order|
|**Use Cases**|Web browsing, email, file transfer|Streaming, online gaming, DNS queries|
### **Use Cases for TCP**

1. **Web Browsing (HTTP/HTTPS)**:  
    When you browse the web, your browser uses TCP to establish a connection with a web server. The reliability of TCP ensures that all website content (text, images, scripts) is delivered correctly and in order.
    
2. **File Transfers (FTP, SFTP)**:  
    TCP is used in file transfer protocols like FTP and SFTP to ensure that large files are transferred accurately without corruption or loss of data.
    
3. **Email (SMTP, IMAP, POP3)**:  
    When sending or receiving email, TCP ensures that the email content and attachments are delivered in full.