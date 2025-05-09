# Networking Basics #1

## Description

This project explores fundamental networking concepts on Ubuntu servers, focusing on IP addressing, network interfaces, and port communication. Through a series of practical exercises, you'll learn about localhost, IP configurations, and basic network communication.

## Learning Objectives

By the end of this project, you will understand:

- What is localhost/127.0.0.1
- What is 0.0.0.0
- What is /etc/hosts
- How to display your machine's active network interfaces
- How to manipulate IP configurations
- How to set up basic port listening

## Concepts Covered

### Localhost (127.0.0.1)

Localhost refers to the current machine you're working on. The IP address 127.0.0.1 is reserved for loopback communication, allowing a device to communicate with itself. This is particularly useful for testing network applications without sending data over a physical network.

### 0.0.0.0

The IP address 0.0.0.0 has multiple meanings depending on the context:

- When used as a destination address, it represents the default route (all network destinations)
- When used as a source address, it means "any IPv4 address at all"
- In server applications, binding to 0.0.0.0 means "listen on all available IPv4 interfaces"

### /etc/hosts File

The hosts file (/etc/hosts) is a system file that maps hostnames to IP addresses. It's used by the operating system to resolve hostnames before querying DNS servers. This file can be modified to override DNS for specific domains or to block websites by redirecting their domains to different IPs.

### Network Interfaces

Network interfaces are connection points between a computer and a network. These can be physical (Ethernet cards, WiFi adapters) or virtual (loopback interface). Understanding how to identify and configure these interfaces is essential for network troubleshooting and configuration.

## Project Tasks

### Task 0: Change your home IP

Write a Bash script that configures an Ubuntu server with the following requirements:

- localhost resolves to 127.0.0.2
- facebook.com resolves to 8.8.8.8

This task demonstrates how to modify the /etc/hosts file to change how your system resolves specific domain names.

### Task 1: Show attached IPs

Write a Bash script that displays all active IPv4 IPs on the machine it's executed on.

This task teaches you how to identify the IP addresses currently in use on your system, which is valuable for network diagnostics and configuration.

### Task 2: Port listening on localhost

Write a Bash script that listens on port 98 on localhost.

This task introduces you to socket programming basics, showing how to create a simple server that listens for connections on a specific port.

## Requirements

- All scripts must be written for Ubuntu 22.04 LTS
- All files must be executable
- Scripts must pass Shellcheck (version 0.7.0) without errors
- The first line of all scripts should be exactly `#!/usr/bin/env bash`
- The second line of all scripts should be a comment explaining what the script does

## Tools and Resources

### Commands to Master

- `ifconfig` - Display or configure network interface parameters
- `telnet` - User interface to the TELNET protocol
- `nc` (netcat) - TCP/IP swiss army knife for networking
- `cut` - Remove sections from each line of files

### Additional Resources

- Understanding localhost/127.0.0.1
- Understanding 0.0.0.0
- Working with the hosts file
- Practical examples with Netcat
- Basic network troubleshooting

## Tips for Success

1. Test your scripts in a controlled environment before applying changes to production systems
2. When modifying the hosts file, be aware that changes can affect the normal operation of your system
3. Always make backups before making significant changes to system files
4. Use `man` pages to understand the full capabilities of the networking tools

## Repository Structure

```
holbertonschool-network/
├── basics_1/
│   ├── 0-change_your_home_IP
│   ├── 1-show_attached_IPs
│   ├── 2-port_listening_on_localhost
│   └── README.md
```
