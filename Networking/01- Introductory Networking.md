# 🌐Introductory Networking - An introduction to networking theory and basic networking tools

## 1. Purpose of this write-up
I completed the Introductory Networking room on TryHackMe to strengthen my cybersecurity fundamentals. This write-up documents my understanding of basic networking concepts in my own words.

## 2. What this room was about
This room covered the following topics : 
- The OSI Model
- The TCP/IP Model
- How these models look in practice
- An introduction to basic networking tools

## 3. Key concepts explained: 

### 3.1 The OSI Model
OSI(Open Systems Interconnection) is a standerised framework that tells how computer networking works in real time. It comprises of 7 layers, each serving their own purpose in networking and communication.

**Layer 7 - The Application Layer**
- Interacts directly with end-user applications.
- Uses protocols such as **HTTP(for web browsing), FTP(for sending files), SMTP(for emails)**
- Serves as a bridge between the user and the application, where user could interact with web browsers, applications and manage various tasks.
- Also responsible for data encoding, representation and session management.
  
**Layer 6 - The Presentation Layer**
- Responsible for translating, formatting, and encrypting data for the application layer.
- *Translates* data into a format that is easy to understand, *converts* data into one format to another, *encrypts* data for ensuring data integrity throughout the transfer process.
- Additionally handles data serialization and deserialization.
  
**Layer 5 - The Session Layer**
- Establishes, manages and terminates connections or *sessions* between applications on different devices.
- When data is received from the presentation layer, the session layer checks if a connection can be established with the target device.
- Manages flow of data within the applications and encourages coordination among the devices for better communication.

**Layer 4 - The Transport Layer**
- Chooses which protocol to be used for data transmission in the network.
- Two most common protocols used here - **TCP & UDP**.
- TCP(Transmission Control Protocol) is mainly used for reliable communication and data transfer within the application, which also guarantees data security and integrity. While UDP(User Datagram Protocol) is connection-less protocol and mainly used for high speed data transfer.
- With a protocol selected, the transport layer then divides the transmission up into bite-sized pieces (over TCP these are called segments, over UDP they're called datagrams), which makes it easier to transmit the message successfully.
 
**Layer 3 - The Network Layer**
- Focuses on Logical Addressing. Its most common form currently being IPV4. 
- When you want to request information from a webpage, it's the network layer that takes the IP address for the page and figures out the best route to take.

**Layer 2 - The Data Link Layer**
- It handles physical addressing using MAC addresses - *(a unique address given to every Network Interface Card (NIC), written in hexadecimal format)*.
- Layer 3 sends a packet with an IP address. Layer 2 then converts the packet into frames and adds the MAC address of the destination device to it.

**Layer 1 - The Physical Layer**
- Lowest layer of the OSI model that deals with the actual hardware(cables, switches, ports).
- Works with Binary data. Converts raw data into electric signals that are transmitted through wired or wireless mediums throughout the network.
- If layer 1 fails, no data transmission would be possible. 
---
### 3.2 ENCAPSULATION 
It is the process of adding extra bit of information to the data as it moves in the OSI model.

**🔁 How Encapsulation Works**
- *Layer 7 -* Original data is created here. An aplication header is added.
- *Layer 6-* Data is compressed, encrypted or formatted. A presentation header is added.
- *Layer 5-* Manages session between sender and receiver. A session header is added.
- *Layer 4-* Data is broken into smaller parts and a Transport header is added based on the protocol used (TCP/UDP)
- *Layer 3-* Data is referred to as packet. Adds source and destination IP address to the data.
- *Layer 2-* Data is referred to as frames. A header and a trailer is added to data. 
- *Layer 1-* Frame is converted into bits (0s and 1s) and then passed in the form of electric signals.

| OSI Layer | Layer Name        | Data Unit Name            |
|----------|-------------------|---------------------------|
| Layer 7  | Application       | Data                      |
| Layer 6  | Presentation      | Data                      |
| Layer 5  | Session           | Data                      |
| Layer 4  | Transport         | Segment (TCP) / Datagram (UDP) |
| Layer 3  | Network           | Packet                    |
| Layer 2  | Data Link         | Frame                     |
| Layer 1  | Physical          | Bits                      |


**🔁 How De-encapsulation Works**
The receiver does the reverse of what was done in encapsulation. The data is sent from layer 1 -> layer 7. In every step, header and trailer is removed from each layer.

**✅ Why Encapsulation is Important?**

- Ensures correct delivery

- Provides error checking

- Allows different devices & OS to communicate

- Follows a standard method for data transfer

> 📌 **Note:** The data link layer is the only layer tha adds a piece on at the end of the transmission, called as trailer, which is used to verify that the data has not been corrupted on transmission. This also has the added bonus of increased security, as the data can't be intercepted and tampered with without breaking the trailer.

---

### 3.3 MAC address
A MAC address is a hardware-level identifier assigned to a network interface. It is used inside local networks for communication.

### 3.4 DNS (Domain Name System)
DNS converts human-friendly website names (like google.com) into IP addresses that computers understand.

### 3.5 TCP vs UDP
- **TCP** ensures reliable communication by checking that data is delivered correctly.
- **UDP** is faster but does not guarantee delivery.

## 4. Commands and tools introduced
The following commands were introduced to observe or test network connectivity:
- `ping`
- `traceroute` / `tracert`
- `ifconfig` / `ipconfig`

These tools help verify connectivity and understand how data travels across networks.

## 5. Why these concepts matter in cybersecurity
Cybersecurity relies heavily on networking because:
- Attacks travel through networks
- Logs and alerts are network-based
- Monitoring traffic is key to detecting threats

Without understanding networking, security analysis becomes difficult.

## 6. What I found confusing initially
Subnetting and understanding how IP ranges work was confusing at first and requires more practice.

## 7. What became clear after completing the room
I now understand:
- How devices identify each other on a network
- How DNS plays a critical role in accessing websites
- Why TCP and UDP are used for different purposes

## 8. My main takeaway
Networking is the foundation of cybersecurity. A strong understanding of networking concepts is necessary before moving deeper into security topics such as monitoring, detection, and incident response.

