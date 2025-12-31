# Project 2 – Homelab Networking and Security Configuration

**Area:** Networking & Security  
**Level:** Intermediate  
**Year:** 2025  

## 1. Description

This project documents the setup, configuration, and troubleshooting of a small homelab environment using reused hardware. A laptop from 2007 was repurposed as a server and managed remotely from a personal computer. The focus of the project was homelab system administration, firewall configuration, remote access, and service accessibility.

## 2. Objective

To deploy and maintain a functional homelab using limited hardware resources, configure secure remote access, manage firewall rules for hosted services, and resolve connectivity and system behavior issues in a server environment.

## 3. Tools and Technologies

- **Hardware:**
  - Desktop PC (used to remotely access and manage the homelab)
  - Laptop (A 2007 laptop reused as a homelab server)
  - USB (To install the OS)

- **Software:**
  - Linux-based operating system (Ubuntu 24.04.3 LTS)
  - Firewall utilities
  - SSH

- **Networking & System Tools:**
  - `ifconfig`
  - `ping`
  - `grep`
  - `cat`
  - `ip a`

## 4. Homelab Configuration

1. Installed and configured a Linux-based operating system on the reused laptop.  
2. Connected the homelab server to the local network via an Ethernet cable and verified IP assignment.  
3. Tested connectivity and service availability using `ping`.  
4. Enabled SSH access to manage the server remotely from the desktop PC.  

## 5. Security Measures Implemented

- Configured firewall rules to control inbound and outbound traffic.  
- Opened and closed specific ports required by homelab services.  
- Restricted unnecessary ports to reduce exposure and improve security.  
- Used SSH for secure remote administration.

## 6. Challenges and Solutions

- **Services Not Accessible Due to Firewall Rules**  
  Services running on the homelab server were unreachable because required ports were blocked. This was resolved by identifying service port requirements and modifying firewall rules accordingly.

- **System Shutdown When Laptop Lid Was Closed**  
  The laptop powered off automatically when the lid was closed. System configuration files were inspected and modified using tools such as `grep` to prevent suspend or shutdown behavior.

- **Performance Constraints of Legacy Hardware**  
  Due to hardware limitations, the laptop display was physically disconnected to reduce resource usage and improve system stability.

- **Battery Failure**  
  The battery was unable to hold a charge, requiring the system to remain permanently connected to an external power source to ensure uninterrupted operation.

## 7. Results

- Successfully deployed a stable homelab server using reused hardware.
- Enabled secure remote management via SSH.
- Restored access to hosted services by correctly configuring firewall rules.
- Achieved reliable long-term operation despite hardware limitations.

## 8. What I Learned

- Homelab deployment and management
- Firewall configuration and port management
- Secure remote access using SSH
- Understanding legacy and modern Linux networking tools (`ifconfig` vs `ip a`)
- Troubleshooting service accessibility issues
- Adapting systems to operate on legacy hardware

## 9. Evidence

### Notes

This homelab project strengthened my understanding of how networking, security, and system configuration interact in real server environments, especially when working with limited or reused hardware.
