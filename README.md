# IT Support Labs

## Overview
This repository contains a collection of hands-on IT support labs focusing on LAN networking, device connectivity, VLAN configuration, network topology design, and firewall basics. All labs are designed for beginners and intermediate learners.

## Topics Covered

### Network Fundamentals
- **LAN Pinging** - Testing connectivity between multiple devices
- **VLAN Configuration** - Creating and managing Virtual Local Area Networks
- **Network Topologies** - Building networks with switches and routers
- **Firewall Basics** - Introduction to firewall rules and network security

## Prerequisites
- Virtual Machine (Linux-based recommended)
- Basic understanding of networking concepts
- Access to network simulation tools or physical lab equipment
- Familiarity with command-line interface

## Quick Linux Commands (For Lab Use)

Quick reference for the essential commands you'll use in your labs:

```bash
# View files and navigate
ls                              # List files
cat filename                    # Display file contents

# Network testing
ping -c 4 192.168.1.1          # Test connectivity to device
ping google.com                # Test internet connectivity

# View network configuration
ip addr show                    # Display network interfaces
ifconfig                        # Alternative to ip addr show
```

## Linux Commands Progression (Complete Reference Guide)

This section is a complete reference guide for anyone learning Linux networking commands. You can use this as needed!

### 1. Basic Navigation & File Management
Before working with networking, ensure you're comfortable with basic Linux commands:

```bash
# Check current directory
pwd

# List files and directories
ls
ls -la          # Detailed listing with hidden files
ls -l           # Long format

# Change directory
cd /path/to/directory
cd ~            # Go to home directory
cd ..           # Go to parent directory

# Create directories
mkdir directory_name

# Copy files
cp source.txt destination.txt
cp -r source_folder/ destination_folder/

# Move/rename files
mv oldname.txt newname.txt
mv file.txt /path/to/destination/

# Remove files/directories
rm filename.txt
rm -r folder_name   # Remove directory and contents

# Display file contents
cat filename.txt
cat -n filename.txt # Display with line numbers
```

### 2. System Information
Check your system configuration before networking labs:

```bash
# Display system information
uname -a

# Check current user
whoami

# Display hostname
hostname

# Check disk space
df -h

# Check available memory
free -h

# Display system uptime
uptime
```

### 3. Networking Fundamentals
Test basic connectivity and view network configuration:

```bash
# Ping a device (test connectivity)
ping -c 4 192.168.1.1         # Send 4 ping packets
ping google.com

# Display network interfaces
ifconfig                        # Older method
ip addr show                    # Modern method

# Check specific interface
ip addr show eth0

# Display routing table
ip route show
route -n

# Check network statistics
netstat -an
ss -an                          # Modern replacement for netstat

# Trace route to destination
traceroute 8.8.8.8
mtr 8.8.8.8                     # More advanced traceroute

# Check DNS resolution
nslookup google.com
dig google.com
```

### 4. Advanced Networking (Reference Guide)
VLAN configuration, routing, and firewall management:

```bash
# View VLAN configuration
cat /proc/net/vlan/config

# Create VLAN interface
sudo ip link add link eth0 name eth0.10 type vlan id 10
sudo ip addr add 192.168.10.1/24 dev eth0.10
sudo ip link set eth0.10 up

# View firewall rules (UFW - Uncomplicated Firewall)
sudo ufw status
sudo ufw status verbose

# Enable/disable firewall
sudo ufw enable
sudo ufw disable

# Add firewall rules
sudo ufw allow 22/tcp           # Allow SSH
sudo ufw allow 80/tcp           # Allow HTTP
sudo ufw allow 443/tcp          # Allow HTTPS
sudo ufw deny 23/tcp            # Deny Telnet

# View iptables rules (advanced firewall)
sudo iptables -L
sudo iptables -L -v -n          # Verbose with numbers
```

## Lab Structure

Each lab is designed to progress from basic to intermediate difficulty:

1. **Basic LAN Pinging** - Confirm connectivity between devices
2. **VLAN Creation** - Configure multiple virtual networks
3. **Switch-Based Networks** - Build networks using switches
4. **Router-Based Networks** - Implement routing between networks
5. **Firewall Basics** - Configure basic firewall rules and policies

## Lab Files

Cisco Packet Tracer `.pkt` files for each lab will be included in this repository. Each file contains the network topology and configurations needed for that specific lab.

## Getting Started

1. Set up your VM or lab environment
2. Use the Quick Linux Commands section for essential commands
3. Refer to the complete reference guide as needed
4. Progress through the lab exercises
5. Document your configurations and results

## Tips for Success

- Start with simple topologies before moving to complex ones
- Always test connectivity after each configuration change
- Document all commands used and their outputs
- Use `man` command for help: `man ifconfig`
- Practice commands multiple times until comfortable

## Requirements

- Virtual Machine or physical lab setup
- Network simulation software (Cisco Packet Tracer, GNS3, etc.)
- Linux environment (Ubuntu, CentOS, Debian, etc.)
- Terminal/Command-line access

---

**Happy Labbing!** 🖥️🔗
