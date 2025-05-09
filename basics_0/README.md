# Networking Fundamentals

This project covers essential networking concepts that are fundamental to understanding how computer networks and the Internet function.

## OSI Model

The Open Systems Interconnection (OSI) model is a conceptual framework used to understand and implement network interactions. It divides network communication into seven distinct layers, each handling specific aspects of data transmission.

### What it is

The OSI model is a reference model developed by the International Organization for Standardization (ISO) that standardizes the functions of a communication system regardless of its underlying technology. It provides a common basis for the coordination of standards development for systems interconnection.

### How many layers it has

The OSI model consists of 7 layers.

### How it is organized

The OSI model is organized into seven layers, from bottom to top:

1. **Physical Layer**: Deals with the physical connection between devices, defining hardware specifications such as cables, pins, voltages.
2. **Data Link Layer**: Provides node-to-node data transfer and handles error detection/correction from the Physical layer.
3. **Network Layer**: Manages packet routing through multiple networks, addressing, and traffic control.
4. **Transport Layer**: Provides end-to-end communication control, ensuring complete data transfer.
5. **Session Layer**: Establishes, manages, and terminates connections between applications.
6. **Presentation Layer**: Translates data between the application layer and the network format, handling encryption, compression, and protocol conversion.
7. **Application Layer**: Directly interacts with software applications, providing network services to application processes.

## What is a LAN

A Local Area Network (LAN) connects computers and devices within a limited area.

### Typical usage

LANs are typically used in homes, schools, and office buildings to share resources like files, printers, and internet connections. They facilitate local communication between connected devices and enable centralized management of resources.

### Typical geographical size

A LAN typically covers a small geographical area, such as a single building, a school, or a group of nearby buildings. The typical range is limited to about 1 kilometer.

## What is a WAN

A Wide Area Network (WAN) connects LANs across large geographical distances.

### Typical usage

WANs are used to connect offices, data centers, and cloud services across cities, countries, or continents. They enable organizations to maintain communication and data sharing between geographically dispersed locations.

### Typical geographical size

WANs cover large geographical areas such as cities, countries, or even continents. They can span anywhere from tens of kilometers to thousands of kilometers.

## What is the Internet

The Internet is a global system of interconnected computer networks that use standardized communication protocols (primarily TCP/IP) to link devices worldwide.

### What is an IP address

An IP (Internet Protocol) address is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves as an identification and location address.

### What are the 2 types of IP address

1. **IPv4 (Internet Protocol version 4)**: A 32-bit address expressed in four decimal numbers (0-255) separated by dots (e.g., 192.168.1.1).
2. **IPv6 (Internet Protocol version 6)**: A 128-bit address expressed in hexadecimal numbers separated by colons (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

### What is `localhost`

`localhost` refers to the current device or computer being used. It corresponds to the IP address 127.0.0.1, which is a loopback address that connects back to the same device, allowing it to communicate with itself.

### What is a subnet

A subnet (short for subnetwork) is a logical subdivision of an IP network. Subnetting divides a large network into smaller, more efficient subnetworks to improve performance, security, and address allocation. It's defined by applying a subnet mask to the IP address.

### Why IPv6 was created

IPv6 was created to address the anticipated exhaustion of IPv4 addresses. With only 4.3 billion possible addresses in IPv4, the exponential growth of internet-connected devices created a need for a vastly expanded address space. IPv6 provides approximately 340 undecillion addresses (3.4 × 10^38), which is considered sufficient for the foreseeable future. Additionally, IPv6 offers improvements in security, routing efficiency, and simplified network configuration.

## TCP/UDP

### What are the 2 mainly used data transfer protocols for IP

The two main data transfer protocols used with IP are:

1. **TCP (Transmission Control Protocol)**
2. **UDP (User Datagram Protocol)**

These protocols operate at the Transport layer (Layer 4) of the OSI model.

### What is the main difference between TCP and UDP

The main difference is that TCP is connection-oriented and provides reliable data delivery, whereas UDP is connectionless and does not guarantee delivery.

TCP establishes a connection before data transfer, ensures all packets arrive in order, and checks for errors with acknowledgments and retransmissions. This makes it suitable for applications where data integrity is critical.

UDP sends data without establishing a connection or verifying delivery, making it faster but less reliable. It's suitable for applications where speed is more important than perfect reliability, such as live streaming or online gaming.

### What is a port

A port is a numerical identifier (ranging from 0 to 65535) that designates a specific process or service on a computer. Ports allow a single computer with one IP address to run multiple services, with each service assigned to a unique port number.

### Memorize SSH, HTTP and HTTPS port numbers

- **SSH (Secure Shell)**: Port 22
- **HTTP (Hypertext Transfer Protocol)**: Port 80
- **HTTPS (HTTP Secure)**: Port 443

### What tool/protocol is often used to check if a device is connected to a network

**ICMP (Internet Control Message Protocol)** is commonly used to check network connectivity, most notably through the `ping` tool. Ping sends ICMP Echo Request packets to the target device and waits for ICMP Echo Reply messages, providing information about whether the device is reachable and the round-trip time for the packets.
