# Basic Networking Lab – Cisco Packet Tracer

Lab Type: End-to-End Connectivity + ARP Resolution  
Tool Used: Cisco Packet Tracer  
Date Completed: May 2025

This lab demonstrates how to build a simple local area network (LAN) using two PCs and a switch. It focuses on assigning IP addresses to end devices, verifying connectivity using ping, and observing how ARP is used to resolve MAC addresses before communication happens.

## Objective:
- Connect two PCs using a switch
- Assign IP addresses
- Test communication with ping
- Observe ARP behavior during communication

## Devices Used:
- 2 PCs
- 1 Switch
- 2 Straight-through Ethernet cables

## Configuration Steps:
1. Connected each PC to the switch using straight-through cables.
2. Assigned the following IP addresses directly on the PCs:
   - PC0: 192.168.1.1 /24
   - PC1: 192.168.1.2 /24
3. From PC0, used the ping command to communicate with PC1.

## What Happened Behind the Scenes:
- When PC0 attempted to ping PC1, it didn’t initially know PC1’s MAC address.
- PC0 sent an ARP Request to ask “Who has 192.168.1.2?”
- PC1 responded with an ARP Reply, providing its MAC address.
- PC0 stored this in its ARP table and then sent the ICMP Echo Request (ping).
- Communication was successful.

## Outcome:
- Ping test confirmed full connectivity.
- ARP entries were dynamically created on both PCs after the first communication.

## How to View ARP:
- On each PC, open the command prompt and run: arp -a
- This displays the current ARP table, showing IP-to-MAC mappings.

## Key Takeaways:
- ARP enables IP-based devices to discover each other’s MAC addresses on a LAN.
- A switch doesn’t need configuration for this—it simply forwards frames based on MAC addresses.
- Understanding ARP helps in diagnosing early-stage connectivity issues.

   first lab README
