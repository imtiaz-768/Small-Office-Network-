# Small-Office-Network-
Small Office Network – Technical Configuration Overview

In this project, I designed and implemented a Small Office Network by subnetting a single network, configuring DHCP services, setting up wireless access, and enabling seamless communication between departments.

**1. Subnetting the Network (192.168.40.0/24 → Two /25 Subnets)**

The main network 192.168.40.0/24 was divided into two equal subnets to separate office departments:

Subnet 1 – Accounts Department

Network: 192.168.40.0/25

Range: 192.168.40.1 – 192.168.40.126

Gateway: 192.168.40.1

Subnet 2 – Delivery Department

Network: 192.168.40.128/25

Range: 192.168.40.129 – 192.168.40.254

Gateway: 192.168.40.129

This segmentation enhances traffic management, security, and IP allocation efficiency.

**2. Router Interface Configuration**

Each subnet was assigned to a router interface:

Gig0/0 → 192.168.40.1/25 (Accounts)

Gig0/1 → 192.168.40.129/25 (Delivery)

The router provides gateway services and handles inter-subnet routing.

**3. DHCP Configuration**

DHCP was enabled on the router to automatically assign IP addresses to all wired and wireless devices:

DHCP Pool 1 – Accounts Dept

Network: 192.168.40.0/25

Default gateway: 192.168.40.1

DNS server (optional): Configured per office setup

DHCP Pool 2 – Delivery Dept

Network: 192.168.40.128/25

Default gateway: 192.168.40.129

Static IPs were reserved for network devices such as switches, printers, and APs.

**4. Switch Configuration**

Each department has a switch that connects:

Desktop PCs

Printers

Wireless Access Points
