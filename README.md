# Packet-tracer-activities
This is where I post my Packet Tracer Network Design Practice to help me practice for CCNA 200-301 exam.
1. VLAN & VLSM
In this packet tracer activity, I created 3 VLANS and using VLSM to separate the networks in order to reduce wasted addresses. VLAN is highly useful to segment a single LAN into multiple LANs (Virtually) to improve network performance, traffic control, and monitoring.

2. Multilayer Switch & OSPF
I replaced one of the access layer switch from previous lab to a Distribution layer switch (A switch that is capable of both routing and switching). This allows us to remove the sub-interfaces on the router and configure Inter-Vlan routing on the DSW instead. It makes traffic to be less congested and easier to manage overall. I also added an external router to simulate the internet which requires routers to share routing infomation with its neighbours. While it's possible to configure it statically, it is very time-consuming and error occurs more frequently. Instead, using a dynamic routing protocol such as OSPF is the better practice, as what I have implemented in this lab. 

3. Etherchannel
Etherchannel allows multiple port to be combined into one virtual port. This increases bandwidth that otherwise would not be possible due to Spanning Tree Protocol(STP), because it will block any other port to prevent broadcast storms (loops) in the network. I configured both LACP and PAgP as methods to bundle multiple ethernet connections as 1 virtual port.

4. HSRP
First Hop Redundancy Protocol allows devices to connect to public/external network even if something goes wrong with the default gateway's connection (i.e. Interface down, etc). This is possible by configuring HSRP (Hot Standby Router Protocol - Cisco Proprietary) on Cisco's routers. It allows a group of routers to configure a Virtual IP that can be used as default gateway for end devices, and in the event of interface failure, HSRP will seamlessly transition the traffic into another healthy router within the group.
   
