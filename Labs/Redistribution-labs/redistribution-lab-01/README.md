## Lab 01 – Multi-Protocol Redistribution (OSPF, EIGRP, RIP)
<h3>1. Objective</h3>

This lab was built to practice route redistribution between three different routing protocols - OSPF, EIGRP, and RIP - using a single central router as the redistribution point. The goal was to make sure that Loopback interfaces on every router (representing "networks" in each domain) are reachable from every other router in the topology, regardless of which routing protocol that router is running.

<h3>2. Topology</h3>
   
   <img width="556" height="259" alt="image" src="https://github.com/user-attachments/assets/16b51945-c6ef-44cd-9117-bc6bdca5c136" />

R1 sits at the center of the topology and is the only router that touches every routing domain. Because of this, R1 is the single Autonomous System Boundary Router (ASBR) responsible for all redistribution in this lab.

<h3>3. Why R1 Is the Redistribution Point</h3>

R1 is the only router with interfaces in all five domains (OSPF-1, RIP, EIGRP-100, EIGRP-200, OSPF-2). Redistribution must happen on R1, because that is the only router where routes from one protocol can be learned and then re-advertised into another.

R2, R3, R4, R5, and R6 are all stub routers - each one only participates in a single protocol domain. Configuring redistribution commands on them has no effect, since they never learn routes from more than one protocol in the first place.

<h3>4. Configuration</h3>
All configurations commands of each router has been added to the configuration.md file.


<h3>5. Verification</h3>
Command outputs and screenshots of each of the devices has been added to the verification commands folder.

<h3>6. Issues Faced & Fixes</h3>
See WHAT-I-LEARNED.md for the full breakdown (mistake → root cause → fix → concept reinforced).

Quick summary: redistribution commands were first applied on R2 and R4, which had no effect since those routers only touch a single protocol domain. The fix was moving all redistribution configuration to R1, the only router with visibility into every domain.







