# Project 4 – Ubuntu Server Installation and Configuration

**Area:** Systems Administration / Operating Systems  
**Level:** Intermediate  
**Year:** 2025  

## 1. Description

This project documents the installation and initial configuration of Ubuntu Server on legacy hardware as part of a personal homelab. The system was deployed in a home environment using a reused laptop and configured to operate as a lightweight server without a graphical interface.

The focus of this project was to install a stable and resource-efficient operating system, configure secure remote access, manage system behavior, and prepare the server to host basic services despite hardware limitations.

## 2. Objective

To install and configure a lightweight Linux server operating system on legacy hardware, enabling secure remote administration, basic networking services, and long-term stability for homelab usage.

## 3. Hardware and Type of Network

- **Device:** Dell Vostro 1500 (2007)
- **RAM:** 2 GB
- **Storage:** 500 GB HDD
- **Network:** Ethernet connection

### Hardware Limitations
- Limited system performance
- Battery no longer holds charge
- Display consumes unnecessary resources
- Only supports 2–3 services running simultaneously

## 4. Tools and Software

- **Operating System:** Ubuntu Server 24.04.3 LTS
- **Boot Media Tool:** BalenaEtcher
- **Access:** BIOS / Boot Menu
- **Terminal utilities:**
  - `ip a`
  - `ping`
  - `journalctl`
  - `nano`

## 5. Installation Process

1. Created a bootable USB drive using balenaEtcher.
2. Accessed the BIOS/Boot Menu using the `F2` key and modified the boot order.
3. Installed Ubuntu Server as a single operating system, removing the previous Windows installation.
4. Configured language, keyboard, network, storage, and user profile.
5. Enabled SSH access during installation.
6. Connected the system to the local network using Ethernet with automatic IP assignment (DHCP).

## 6. Initial System Configuration

After installation, the following configurations were performed:

- Updated the system packages.
- Verified network configuration using `ip a`.
- Tested external connectivity using `ping` to public servers.
- Enabled and configured SSH for remote administration.
- Configured firewall rules to control open and close ports.
- Modified system behavior to prevent shutdown when closing the laptop lid by editing:

  ```bash
  /etc/systemd/logind.conf
  ```
  
### 7. Challenges and Solutions

- **Firewall Configuration Issues**
Some hosted services were initially inaccessible due to closed ports. This was resolved by identifying required ports and adjusting firewall rules accordingly.

- **System Shutdown When Closing the Lid**
The laptop powered off when the lid was closed. This behavior was resolved by researching systemd power management and modifying configuration files to disable lid-triggered suspend actions.

- **Battery Failure**
The battery could not hold a charge. This limitation was mitigated by keeping the system permanently connected to external power.

### 8. Results

- Successfully deployed a stable Ubuntu Server system on legacy hardware.
- Enabled secure remote access via SSH.
- Configured firewall rules to allow hosted services.
- Prepared the system to host lightweight services such as:
  - IT tools service
  - Resource monitoring service
  - Network monitoring service
  - VPN (WireGuard)
  - Cloudflare tunnel for external access

### 9. What I Learned

- Linux server installation and configuration
- Boot process and BIOS configuration
- System administration on resource-limited hardware
- Firewall configuration and port management
- Secure remote access using SSH
- Power management and system behavior control
- Reusing hardware efficiently instead of replacing it

### 10. Evidence

### Reflection

This project demonstrates initiative and commitment to informatics by reusing legacy hardware instead of acquiring new equipment. Overcoming hardware limitations required independent research, experimentation, and problem solving. The experience strengthened my understanding of operating systems, system administration, and practical server deployment in real world conditions.
