<h2>Lab 01 – Multi-Protocol Redistribution (OSPF, EIGRP, RIP)</h2>
<h3>1. Objective</h3>

This lab was built to practice route redistribution between three different routing protocols - OSPF, EIGRP, and RIP - using a single central router as the redistribution point. The goal was to make sure that Loopback interfaces on every router (representing "networks" in each domain) are reachable from every other router in the topology, regardless of which routing protocol that router is running.

<h3>2. Topology</h3>
   
   <img width="556" height="259" alt="image" src="https://github.com/user-attachments/assets/16b51945-c6ef-44cd-9117-bc6bdca5c136" />

R1 sits at the center of the topology and is the only router that touches every routing domain. Because of this, R1 is the single Autonomous System Boundary Router (ASBR) responsible for all redistribution in this lab.

<h3>3. Why R1 Is the Redistribution Point</h3>

R1 is the only router with interfaces in all five domains (OSPF-1, RIP, EIGRP-100, EIGRP-200, OSPF-2). Redistribution must happen on R1, because that is the only router where routes from one protocol can be learned and then re-advertised into another.

R2, R3, R4, R5, and R6 are all stub routers - each one only participates in a single protocol domain. Configuring redistribution commands on them has no effect, since they never learn routes from more than one protocol in the first place.

<h3>4. Configuration</h3>
<b>4.1 R1 (Redistribution Router)</b>

<img width="590" height="314" alt="image" src="https://github.com/user-attachments/assets/d3ac4afd-b372-49f6-b67f-db471bfa6314" /><br>
<img width="407" height="314" alt="image" src="https://github.com/user-attachments/assets/2b31c755-df3e-4e0e-9069-eb37b8580ed3" /><br>
<img width="395" height="175" alt="image" src="https://github.com/user-attachments/assets/bdca31dd-984f-4c08-a090-8099ae63d4ab" /><br>


<b>4.2 R2 – EIGRP 200 (Stub)</b>  <br>
<img width="203" height="52" alt="image" src="https://github.com/user-attachments/assets/7e53f5d7-183f-4a01-9ca2-b5ca3731105f" /> <br>


<b>4.3 R3 – EIGRP 100 (Stub)</b>   <br>
<img width="217" height="52" alt="image" src="https://github.com/user-attachments/assets/cd4e9c81-d266-4a31-965d-2494c749fe82" /><br>


4.4 R4 – OSPF-2 (Stub)<br>
<img width="299" height="79" alt="image" src="https://github.com/user-attachments/assets/851ae1d8-a657-4b69-b533-9d03ba766b12" /><br>

<b>4.5 R5 – OSPF-1 (Stub)</b> <br>
<img width="241" height="67" alt="image" src="https://github.com/user-attachments/assets/9c50e93d-bc06-4d03-8d1f-d06e00d76ca1" /><br>

<b>4.6 R6 – RIP (Stub)</b> <br>
<img width="173" height="68" alt="image" src="https://github.com/user-attachments/assets/b76e3590-06cc-4624-ad9e-6bc57496df86" /><br>

<h3>5. Verification</h3>
Command outputs and screenshots of each of the devices has been added to the verification commands folder.

<h3>6. Issues Faced & Fixes</h3>
See WHAT-I-LEARNED.md for the full breakdown (mistake → root cause → fix → concept reinforced).

Quick summary: redistribution commands were first applied on R2 and R4, which had no effect since those routers only touch a single protocol domain. The fix was moving all redistribution configuration to R1, the only router with visibility into every domain.







