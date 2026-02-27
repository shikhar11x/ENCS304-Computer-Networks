ENCS304 – Computer Networks
Assignment 1: Implementation and Analysis of Basic Network Topologies

Name: Shikhar Bajpai
Roll No.: (Apna roll number daal de)
Programme: B.Tech Computer Science & Engineering
Section: (Apni section daal de)
Date: 27 February 2026

📁 Submitted Files
File Name	Description
exp1_topologies.pkt	Packet Tracer file containing all configured network topologies
output_exp1.txt	Ping outputs and detailed observations
report_exp1.pdf	Complete report including screenshots and analysis
README.md	Instructions to open and test the simulation
🛠️ Software Requirement

Cisco Packet Tracer (Version 8.0 or above recommended)

No additional configuration required

Simulation runs completely inside Packet Tracer

🚀 Steps to Open the Project

Install and open Cisco Packet Tracer

Click File → Open

Select exp1_topologies.pkt

All four topologies are arranged and labelled inside the workspace

🔬 Experiment Details
🔹 Task 1 – Star Topology Using Switch

Devices Used: 1 Switch (2960-24TT) + 4 PCs
Network: 10.10.10.0/24

IP Addressing
Device	IP Address	Subnet Mask
PC0	10.10.10.1	255.255.255.0
PC1	10.10.10.2	255.255.255.0
PC2	10.10.10.3	255.255.255.0
PC3	10.10.10.4	255.255.255.0
Testing Procedure

Open PC0 → Desktop → Command Prompt

Run:

ping 10.10.10.2
ping 10.10.10.3
ping 10.10.10.4
Result

All devices communicated successfully with zero packet loss.
The switch dynamically learned MAC addresses and forwarded traffic only to the required destination port after initial communication.

🔹 Task 2 – Hub-Based Topology

Devices Used: 1 Hub + 4 PCs
Network: 10.10.10.11 – 10.10.10.14

IP Addressing
Device	IP Address	Subnet Mask
PC0	10.10.10.11	255.255.255.0
PC1	10.10.10.12	255.255.255.0
PC2	10.10.10.13	255.255.255.0
PC3	10.10.10.14	255.255.255.0
Testing Procedure

Use Simulation Mode

Send pings from PC0 to other PCs

Observation

All nodes were able to communicate.
However, in simulation mode it was observed that the hub forwards incoming frames to every connected device, increasing broadcast traffic. This makes hub-based networks less efficient compared to switch-based networks.

🔹 Task 3 – Ring-like Topology (Switch Loop with STP)

Devices Used: 3 Switches connected in loop + PCs
Network: 10.10.10.21 – 10.10.10.23

Testing Procedure

Send ping between PCs connected to different switches

Observe STP behaviour

Observation

Communication was successful across multiple switches.
Spanning Tree Protocol automatically disabled one redundant link to prevent looping. The topology remained stable and prevented broadcast storms.

🔹 Task 4 – Link Failure Test
Procedure

Remove one inter-switch cable

Wait for STP to reconverge

Repeat ping test

Observation

After disconnecting a link, communication resumed through the alternate path.
This demonstrates redundancy and improved fault tolerance compared to a simple star topology.

📊 Concepts Verified

Difference between Switch and Hub data forwarding

MAC address learning in switches

Broadcast behaviour in hubs

Loop prevention using Spanning Tree Protocol (STP)

Fault tolerance in ring topology

📌 Conclusion

Through practical simulation in Cisco Packet Tracer, different network topologies were implemented and analyzed.

The switch-based star topology provided better efficiency compared to the hub-based network.
The ring topology with STP demonstrated fault tolerance by maintaining connectivity even after link failure.

This experiment helped in understanding real-world LAN design principles and topology selection based on performance and reliability.
