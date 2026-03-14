# Enterprise Network Infrastructure Lab (IPv4 / IPv6)

This project is a comprehensive enterprise network simulation built using Cisco Packet Tracer.
The goal of this lab is to practice real-world network infrastructure design including routing, switching, network segmentation, redundancy, and security features.

The topology simulates multiple office branches connected through routers and central switches with both IPv4 and IPv6 networking implemented.

---

# Network Topology

This network contains multiple office networks connected through routers and central switching infrastructure.

The design includes:

* Core / central switching
* Multiple branch offices
* VLAN segmentation
* Inter-VLAN routing
* Layer 2 and Layer 3 security features
* Dynamic and static routing
* IPv4 and IPv6 dual-stack configuration

---

# Technologies and Protocols Implemented

## Layer 3 (Routing)

### IPv4 & IPv6 Configuration

All routers are configured with both IPv4 and IPv6 addressing.

Features implemented:

* IPv4 addressing with subnetting and VLSM
* IPv6 addressing and routing
* Dual-stack networking

---

### OSPF & OSPFv3

Dynamic routing is configured using:

* **OSPF (IPv4)**
* **OSPFv3 (IPv6)**

Design characteristics:

* Multiple OSPF Areas

  * Area 0
  * Area 1
* Passive interfaces
* Point-to-point network configuration
* DR / BDR priority configuration
* Loopback interfaces used for router identification

---

### Static Routing

Additional routing features:

* Floating static routes for redundancy
* Backup route configuration

---

# Network Addressing

The topology uses **VLSM and subnetting** to efficiently allocate IP address space.

Features implemented:

* Variable Length Subnet Mask (VLSM)
* Subnet segmentation for each office network
* Separate VLAN subnets

---

# VLAN & Inter-VLAN Routing

Network segmentation is implemented using VLANs.

### VLAN Configuration

Examples include:

* VLAN 100 – User network
* VLAN 200 – Admin network
* VLAN 101 / 201 in Office2

---

### Trunking

Switch-to-switch and switch-to-router connections use:

* **802.1Q trunking**

Native VLAN was modified for security.

---

### Router on a Stick (ROAS)

Inter-VLAN routing is implemented using:

* Subinterfaces on routers
* VLAN tagging

This allows communication between VLANs and access to shared resources such as DHCP servers.

---

# DHCP Implementation

Dynamic IP address assignment is configured.

Features:

* DHCP services configured on routers
* DHCP pools for each office network
* DHCP relay for remote VLANs

Offices with DHCP:

* Office 1
* Office 2
* Office 3

---

# Network Security Features

## Port Security

Implemented on access switch ports.

Configuration includes:

* Maximum MAC address = 2
* Sticky MAC address learning
* Violation mode: **restrict**

This prevents unauthorized devices from connecting to the network.

---

## DHCP Snooping

Used to prevent rogue DHCP servers.

Switches are configured with:

* Trusted ports
* Untrusted ports

---

## Dynamic ARP Inspection (DAI)

Used to prevent ARP spoofing attacks.

DAI validates ARP packets against DHCP snooping bindings.

---

## BPDU Guard & PortFast

Rapid Spanning Tree is implemented with additional protection mechanisms.

Features include:

* PortFast on access ports
* BPDU Guard enabled on edge ports
* Protection against rogue switches

---

# Spanning Tree

The network uses:

**Rapid Spanning Tree Protocol (RSTP)**

Benefits:

* Faster convergence
* Loop prevention
* Network redundancy support

---

# EtherChannel

Link aggregation is configured between switches.

Features:

* EtherChannel / Port aggregation
* Increased bandwidth
* Redundancy between core switches

Configured on:

* Central switch
* Office2 switches

---

# Network Services

## NAT Configuration

Two types of NAT are implemented.

### PAT (Port Address Translation)

Used in:

* Office1

Allows multiple internal hosts to share a single public IP.

---

### Dynamic NAT

Configured in:

* Office2

Maps private addresses dynamically to a pool of public addresses.

---

## Access Control Lists (ACL)

ACLs are configured on:

* Office3 router

Purpose:

* Control network traffic
* Restrict access between network segments

---

## SNMP

Simple Network Management Protocol is enabled on all routers.

Configuration:

* RO (Read Only)
* RW (Read Write)

Allows network monitoring and management.

---

## NTP

Network Time Protocol is configured to synchronize system time across devices.

---

## SSH / Telnet Management

Remote management is enabled on routers.

Features:

* SSH access
* Telnet access
* Local authentication
* RSA key generation (1024-bit)

---

# Switch Layer 2 Features

Switch configuration includes:

* VLAN segmentation
* Trunking
* EtherChannel
* Rapid Spanning Tree
* DHCP Snooping
* Dynamic ARP Inspection
* Port Security

---

# Discovery Protocol

**LLDP** is enabled to allow devices to discover neighboring network devices.

---

# Key Networking Concepts Demonstrated

This lab demonstrates practical implementation of:

* Enterprise network segmentation
* Redundancy and high availability
* Layer 2 and Layer 3 security
* Routing protocols
* IPv4 / IPv6 dual-stack networks
* Network automation readiness

---

# Tools Used

* Cisco Packet Tracer
* Cisco IOS CLI
* Network simulation and testing tools

---

