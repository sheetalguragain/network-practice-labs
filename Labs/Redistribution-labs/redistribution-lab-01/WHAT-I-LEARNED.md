# What I Learned – Lab 01: Multi-Protocol Redistribution

This file documents real mistakes made during this lab, why they happened, how they were fixed, and what concept each mistake reinforced. Format: **Mistake → Root Cause → Fix → Concept Reinforced**.

---

## Entry 1: Redistribution configured on the wrong routers (R2 and R4)

**Mistake:**
Route redistribution commands were first applied on R2 and R4, expecting this to make routes flow between the different protocol domains (EIGRP-200 on R2, OSPF-2 on R4).

**Root Cause:**
R2 and R4 are stub routers - each one only has an interface in a *single* routing domain (R2 is only in EIGRP-200, R4 is only in OSPF-2). A router can only redistribute routes *between* protocols it is actually running. Since R2 and R4 each run just one protocol, there was nothing for them to redistribute - they had no second protocol to pull routes from or push routes into.

**Fix:**
Looked at the topology again and identified that R1 is the only router with interfaces in all five domains (OSPF-1, RIP, EIGRP-100, EIGRP-200, OSPF-2). Moved all `redistribute` statements to R1, under each of its routing processes, so R1 could take routes learned from one protocol and re-advertise them into the others.

**Concept Reinforced:**
Redistribution has to happen on the router that sits at the **boundary between two or more routing protocols** - the ASBR (Autonomous System Boundary Router) for that boundary. A router that only speaks one protocol has no boundary to redistribute across, no matter what commands are typed on it. Before configuring redistribution, always trace the topology first and ask: *"Which router actually touches more than one protocol?"* That router is where the `redistribute` commands belong.



