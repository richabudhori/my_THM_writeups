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

**1. Layer 7 - The Application Layer**
- Interacts directly with end-user applications.
- Uses protocols such as **HTTP(for web browsing), FTP(for sending files), SMTP(for emails)**
- Serves as a bridge between the user and the application, where user could interact with web browsers, applications and manage various tasks.
- Also responsible for data encoding, representation and session management.

**2. Layer 6 - The Presentation Layer**
- 
**1. Layer 7 - The Application Layer**
**1. Layer 7 - The Application Layer**
**1. Layer 7 - The Application Layer**
**1. Layer 7 - The Application Layer**
**1. Layer 7 - The Application Layer**

### 3.2 IP address
An IP address is a unique identifier assigned to a device on a network. It helps data know where to go and where it came from.

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

