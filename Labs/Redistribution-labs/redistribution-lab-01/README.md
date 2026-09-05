## Lab 01 – Multi-Protocol Redistribution (OSPF, EIGRP, RIP)
### 1. Objective

This lab was built to practice route redistribution between three different routing protocols - OSPF, EIGRP, and RIP - using a single central router as the redistribution point. The goal was to make sure that Loopback interfaces on every router (representing "networks" in each domain) are reachable from every other router in the topology, regardless of which routing protocol that router is running.

### 2. Topology

  ![Network Topology](https://github.com/user-attachments/assets/16b51945-c6ef-44cd-9117-bc6bdca5c136)

R1 sits at the center of the topology and is the only router that touches every routing domain. Because of this, R1 is the single Autonomous System Boundary Router (ASBR) responsible for all redistribution in this lab.

### 3. Why R1 Is the Redistribution Point

R1 is the only router with interfaces in all five domains (OSPF-1, RIP, EIGRP-100, EIGRP-200, OSPF-2). Redistribution must happen on R1, because that is the only router where routes from one protocol can be learned and then re-advertised into another.

R2, R3, R4, R5, and R6 are all stub routers - each one only participates in a single protocol domain. Configuring redistribution commands on them has no effect, since they never learn routes from more than one protocol in the first place.

### 4. Configuration
All configurations commands of each router has been added to the [configuration.md](https://github.com/sheetalguragain/network-practice-labs/blob/master/Labs/Redistribution-labs/redistribution-lab-01/configuration.md) file.


### 5. Verification
Command outputs of each of the devices has been added to the [verification.md](https://github.com/sheetalguragain/network-practice-labs/blob/master/Labs/Redistribution-labs/redistribution-lab-01/verification.md) file.

### 6. Issues Faced & Fixes
See [WHAT-I-LEARNED.md](https://github.com/sheetalguragain/network-practice-labs/blob/master/Labs/Redistribution-labs/redistribution-lab-01/WHAT-I-LEARNED.md) for the full breakdown (mistake → root cause → fix → concept reinforced).

Quick summary: redistribution commands were first applied on R2 and R4, which had no effect since those routers only touch a single protocol domain. The fix was moving all redistribution configuration to R1, the only router with visibility into every domain.

### 7. Future Updates

 As I continue learning and practicing, I may come across new concepts or find areas that need to be changed or improved. Any new learnings, corrections, or updates will be added to this repository in the future.






