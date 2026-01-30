# Dual-Stack-VLAN-Networks-for-Branch-Office
This project designs a secure branch office network with VLANs, Router-on-a-Stick inter-VLAN routing, dual-stack IPv4/IPv6 support, router as DHCP, trunking, and basic security to ensure efficient, safe communication across all departments

<body>

<h2>🏢Network Design</h2>
<p>
	•	1 Router (Gateway, DHCP, Inter-VLAN routing)<br>
	•	2 Switches (VLANs, Trunking)<br>
	•	4 VLANs: Sales, Engineering, Guest, HR
  </p>
<p><img src="https://imgur.com/t5nByqz.jpg">
	<img src="https://imgur.com/tdvCev5.jpg">
   <img src="https://imgur.com/si90WYR.jpg">
</p>

<h2>🌐Addressing & Routing</h2>
<p>
  •	IPv4: 172.16.0.0/23 (VLSM applied)<br>
	•	IPv6: Unique /64 per VLAN<br>
	•	Router-on-a-Stick used for inter-VLAN communication

The IPv4 network used is 172.16.0.0/23.
Instead of wasting IP addresses, I applied VLSM (Variable Length Subnet Masking) to allocate IP ranges based on each VLAN’s size.

Why VLSM?
VLSM allows efficient use of IP addresses by assigning smaller or larger subnets depending on the number of hosts required in each VLAN.”
Each VLAN was also assigned a unique IPv6 /64 prefix, which is the standard size for IPv6 LANs.
This ensures future readiness and supports modern networking requirements.

Since multiple VLANs exist, devices in different VLANs cannot communicate by default.
To solve this, I used Router-on-a-Stick, where a single router interface is divided into multiple sub-interfaces, each tagged with a VLAN ID.”Each sub-interface has its own IPv4 and IPv6 gateway address, allowing controlled communication between VLANs.
	
</p>

<p><img src="https://imgur.com/hTwbMky.png">
   <img src="https://imgur.com/G9nlGAs.png">
</p>


 <h2>🔐Security Features</h2>
 <p>
	•	Device passwords and MOTD banner<br>
	•	SSH for remote management<br>
	•	Port Security on Sales, Engineering, and HR ports

Basic device security was implemented by configuring console and VTY passwords, enabling password encryption, and setting a MOTD banner to warn unauthorized users.
	
SSH Configuration
SSH was configured on the router to allow secure remote management instead of Telnet, which sends credentials in plain text.

SSH encrypts traffic, making it more secure than Telnet.

Port Security

Port security was enabled on Sales, Engineering, and HR switch ports to limit the number of devices that can connect.
If an unauthorized device is plugged in, the port either shuts down or restricts access.

</p>
<p><img src="https://imgur.com/4r6qZ0m.png">
   <img src="https://imgur.com/Y0lFkK7.png">
	<img src="https://imgur.com/XWYUVMI.png">
	<img src="https://imgur.com/UxOv46D.png">
</p>

<h2>🧪 Testing</h2>
<p>
	•	Successful IPv4 & IPv6 pings between VLANs<br>
	•	Internet reachability via simulated loopback<br>
	•	Port security violation tested
</p>
<p><img src="https://imgur.com/NaGKCrW.png">
   <img src="https://imgur.com/8hyszIS.png">
   <img src="https://imgur.com/xqQaBaI.png">
</p>

  

<h2>🛠️ Tool Used</h2>
<p>
	•	Cisco Packet Tracer

</p>
<p><img src="https://imgur.com/u7F4vg3.png">
</p>
<h2>Conclusion</h2>

<p>
This project demonstrates the successful design and implementation of a secure dual-stack branch office network using Cisco Packet Tracer. By combining VLAN segmentation, VLSM-based addressing, inter-VLAN routing, DHCP on a router, and security best practices, the network is scalable, efficient, and secure. The project reflects real-world enterprise networking concepts and provides a solid foundation for further expansion.

<p></p>

<body/>


