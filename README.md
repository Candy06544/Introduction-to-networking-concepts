# Introduction-to-networking-concepts
 # Networking Basics: OSI and TCP/IP Models

## Introduction
Networking is important  for modern communication, enabling devices to share data efficiently. Two key models that describe how data is transmitted are the **OSI Model** and the **TCP/IP Model**.

---

## OSI Model

### Overview
The **OSI (Open Systems Interconnection) Model** is a conceptual framework that standardizes the functions of a communication system into seven layers. Each layer has a specific role in processing data for network transmission.

### Layers of the OSI Model


1. **Physical Layer**  
    -Involves connector and interface specifications as well as medium requirements.It is resposible for the following:
   
    1.Transmission of Data:
    - Converts data into electrical signals, light pulses, or radio waves depending on the medium (e.g., copper cables, fiber optics, or wireless).
    - Example: Transmitting raw binary data over a network.
   2.Physical Media
    - Manages the physical equipment used for communication, like cables, connectors, and network interface cards (NICs).
   3.Specifications
    - Defines how devices physically connect, including voltage levels, timing, and data rates.
    - Example: Transmitting raw binary data over a network.

2. **Data Link Layer**  
   - Receives data packets thact contains receiver andsendr adresses
   - Responsible for physical addressing which refers to MAC addresses being assigned to data packets froming a frame 
   - MAC address is a 12 digit alphanumeric number embedded in the NIC card 
   - Data link layer is embedded into the NIC as a software and provide means to transport data from one computer to onother through the local meadia e.gcopper wire,optical 
    fibres and radio signals.
   - Allows upper layers of the OSI to acces the media using techinues such as framing e.g  Example: Ethernet frames.
   -Controls how data is placed and receuved from the media using techniques such as Media Acess Control and error detection.

3. **Network Layer**  
   - Recieves segments from the transport layer and is  responsible for the following:
     
   1. Logical adressing 
   - Every computer has unique IP addresses which is a unique identifier of the computer onthe internet
   - Network layer assings Senders and receiver's  IP address to a segment forming a packet .
   
   2. Routing 
   - Method of removing data packets into source and destination
   - Based on logical addressing  of IPv4 & IPv6 and Mask they ensure that data reaches the correct destination.

   3. Path determination
   - Refers to choosint the right path for data delivery 
   - protocls used for path determination include:

   1. OSPF (Open Shortest Path First) - Like finding the fastest route within your city (intra-city routing).
   2. BGP(Border Gateway Protocol) -Like deciding which highways to take when traveling between cities (inter-city routing).
   3. IS-IS (Intermediate System to Intermediate System) - Like another navigation system for large cities, used for special cases where OSPF might not be ideal.

   
4. **Transport Layer**  

   - Offers end to end communication between end devices through a network in the following ways.
     
   1. Segmentation
   - Data is broken into small data units called segments.Each segments contains source and destionation number,port and sequence number.
   - The port number helps directs each segment to correct application while each sequence number reassemble into correct order to form the correct message.
     
   2. Flow control
   - Controls the flow of data e.g a server can process dat at 100 Mbps while a phone can process data  at 10Mbps. A mobile phone with the help of the transport layer  can 
     tell the server to slow down data transfer into 10 Mbps.
     
   3. Error control
   - sends an aoutomatic repeat request for any missing data
   - A group of bits called checksum is added to each segment to receive and update segments.
     
   4. Connection oriented  transmission 
   - This is through the Tranfer Control Protocol (TCP)
   - TCP provides feedback hence lost data can be retrieved since full data transmission is a must 
   - TCP is mainle used in Emails ,World Wide Web
     
   5. connectionless Transmission
   - This is through the User Datagram Protocol (UDP)
   - Its faster than TCP but doesn't provide feedback hence not all data is recieved ,used mainle in online streaming movies and online games.
   

5. **Session Layer**  
   - Responsible for establishing,managing and terminating sessions between applications .
   - The session layer is responsible for keeping track of the session and With the help of API (application prograamming interface) e.g NetBIOS for communication  
     exchange. 
   - It also helps in authorization and authentication of users for certain information from the server.
   - Example: Keeping an FTP connection open.

6. **Presentation Layer**  
   - Receives data from the application layer inform of  characters and numbers.
   - Data received undergoes three processes
     
    1. Translation
   - The data recived inform of characters and numbers is converted into binary fromat (1,0) understood by the computer.
     
    2. Data compression 
   - Data is compressed reducing the number of bits  so that it ttavels efficiently
     
    3. Encryption /Decryption
  - Data is encrypted at the senders side and decrypted at the reciever side to enhance security .The Secure Socket Layer protocla is used for encryption and decryyption of 
    data.  
   - Example: Converting text to ASCII or encrypting files.

7. **Application Layer**
   
   - The interface between the network and the end-user applications and the layer the user interacts with.
   - Application layer provides services for network application , it also icludes protocolos that aid in the implementation of this services.
   - example :

   1. File Transfer Protocol (FTP) - file transfer
   2. Simple Mail Transfer Protocol (SMTP) - Emails
   3. Hypertext Transfer Protocol /Secure (HTTPS) - Web surfing
   4. Telnet - virtual terminals
   

---

## TCP/IP Model

### Overview
The **TCP/IP (Transmission Control Protocol/Internet Protocol) Model** is a simplified framework used in real-world networking. It consists of four layers that map loosely to the OSI model.

### Layers of the TCP/IP Model
1. **Link Layer (Network Access)**
   
   - Corresponds to the OSI's Physical and Data Link layers.  
   - Handles physical transmission of data between devices.  
   - Technologies: Ethernet, Wi-Fi, ARP (Address Resolution Protocol).
   - Handles data transfer between adjacent devices on the same network.  
   - Example: Ethernet or Wi-Fi.

3. **Internet Layer**
   
   -Responsible for logical addressing and routing.  
   - Core protocols:  
     - **IP (Internet Protocol)**: Assigns unique addresses to devices (IPv4 and IPv6).  
     - **ICMP (Internet Control Message Protocol)**: Handles error reporting and diagnostics.  
   - Manages logical addressing and routing.  
   - Example: IP addressing and routing.

5. **Transport Layer**
   
    - Provides end-to-end communication and data integrity.  
    - Core protocols:
      
     - **TCP (Transmission Control Protocol)**: Reliable, connection-oriented communication.  
     - **UDP (User Datagram Protocol)**: Faster, connectionless communication for real-time applicationS
       
   - Ensures reliable or connectionless data delivery.  
   - Example: TCP for reliable delivery, UDP for faster, connectionless communication.

7. **Application Layer**
   
   - Interfaces directly with user applications for data exchange.  
   - Protocols: HTTP, FTP, DNS, SMTP, and others.

---

## Comparison: OSI vs. TCP/IP

| **Feature**        | **OSI Model**                   | **TCP/IP Model**               |
|---------------------|---------------------------------|---------------------------------|
| **Number of Layers**| 7                               | 4                               |
| **Purpose**         | Theoretical framework          | Practical implementation       |
| **Examples**        | Abstract representation        | Real-world protocols like TCP/IP |

---

## IP Addresses
-Internet Protocola address are unique numbers used to identify a computer on a network.
-Classified in different ways :
1. according to version
IPv4 and IPv6

-IPv4
- Was the previous version of addressing where each group is separated by a period is called an octet
- IP address are converted into binary format through a 8 bit octet chart
- IPv4 adresses are also known as a 32 Bit  adress

### IPv4
- Was the previous version of addressing where each group is separated by a period is called an octet
- IP address are converted into binary format through a 8 bit octet chart
- IPv4 adresses are also known as a 32 Bit  adress 
- **Classes:** A, B, C, D, E for different purposes.  
- **Limitation:** Limited to ~4.3 billion addresses.

### IPv6
- A group of 8 hexadecimal numbers separated by colons 
- Each hexadecimal converts 4 bits 
- **Format:** Hexadecimal notation (e.g., `2001:0db8:85a3::8a2e:0370:7334`).  
- **Advantage:** Supports a vastly larger address space.

### Static and Dynamic IP addresses
- Static IP adresses are provided by the ISP (internet service provider ) and changes when ones uses the network again
- Static IP adresses this are permanent and used by the DNS  (Domain Name System) servers and is easily traceable

### Public and private 
- 1. Public IP Addresses
A public IP address is an address that is accessible over the internet. It allows devices to communicate with other devices on different networks, such as websites, servers, or other computers.

Characteristics of Public IP Addresses:

- Unique Globally- Each public IP is unique across the internet.
- Assigned by ISPs: Internet Service Providers (ISPs) assign public IPs to devices.
- Direct Access: Devices with public IPs can be accessed from anywhere on the internet (if not protected by firewalls).
Examples: 8.8.8.8 (Google's DNS), 142.250.68.78 (Google server).

Use Case:
Hosting websites.
Providing internet access to home networks.
Communication between global systems.

2. Private IP Addresses
A private IP address is used within a local area network (LAN) and is not accessible directly over the internet. These addresses are used for communication within private networks, like homes or businesses.

-Characteristics of Private IP Addresses:

- Not Globally Unique: Devices on different private networks can have the same private IP.
- Defined Ranges: Private IPs fall within these ranges:
- 10.0.0.0 to 10.255.255.255 (Class A)
- 172.16.0.0 to 172.31.255.255 (Class B)
- 192.168.0.0 to 192.168.255.255 (Class C)
- Cannot Access the Internet Directly: Requires Network Address Translation (NAT) to communicate with the internet.
- Use Case:
- Connecting devices like printers, computers, and smartphones within a home or office network.
- Ensuring security by isolating internal devices from the public internet.


 

---

## Example Data Flow
1. A user sends an email via a client (Application Layer).  
2. Data is encrypted and formatted (Presentation Layer).  
3. A session is established (Session Layer).  
4. The message is segmented into packets (Transport Layer).  
5. IP addresses are assigned for routing (Network/Internet Layer).  
6. Data is converted into frames (Data Link Layer).  
7. Bits are transmitted over the physical medium (Physical/Link Layer).  

---

