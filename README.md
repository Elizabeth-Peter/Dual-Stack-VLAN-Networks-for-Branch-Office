# Dual-Stack-VLAN-Networks-for-Branch-Office
This project designs a secure branch office network with VLANs, Router-on-a-Stick inter-VLAN routing, dual-stack IPv4/IPv6 support, router as DHCP, trunking, and basic security to ensure efficient, safe communication across all departments

<body>

<h2>🏢Network Design</h2>
<p>
	•	1 Router (Gateway, DHCP, Inter-VLAN routing)<br>
	•	2 Switches (VLANs, Trunking)<br>
	•	4 VLANs: Sales, Engineering, Guest, HR
  </p>
<p><img src="https://imgur.com/tdvCev5.jpg">
   <img src="https://imgur.com/t5nByqz.jpg">
   <img src="https://imgur.com/si90WYR.jpg">
</p>

<h2>🌐Addressing & Routing</h2>
<p>
  •	IPv4: 172.16.0.0/23 (VLSM applied)<br>
	•	IPv6: Unique /64 per VLAN<br>
	•	Router-on-a-Stick used for inter-VLAN communication
</p>

<p><img src="https://imgur.com/hTwbMky.png">
   <img src="https://imgur.com/G9nlGAs.png">
</p>


 <h2>🔐Security Features</h2>
 <p>
	•	Device passwords and MOTD banner<br>
	•	SSH for remote management<br>
	•	Port Security on Sales, Engineering, and HR ports

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


