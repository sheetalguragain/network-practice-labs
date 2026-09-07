# Network Practice Labs

A collection of hands-on networking labs, built and tested in PNetLab / GNS3-style virtual environments. Each lab is documented with topology diagrams, real configuration, verification steps, and a WHAT-I-LEARNED file covering mistakes made and concepts reinforced along the way.

This repo is a record of practical, self-driven practice following networking training completed in the **CompTIA Network+**, **CCNA**, and **RHCSA** bootcamps under Jiwan Bhattarai Sir. Everything here is real, hands-on work - not certifications, just genuine practice, documented honestly.

## Lab Categories

| Category | Description | Folder |
|----------|-------------|--------|
| DHCP Labs | DORA process, DHCP Relay across routed boundaries, multi-server DHCP scenarios | [`dhcp-labs/`](https://github.com/sheetalguragain/network-practice-labs/tree/master/Labs/DHCP%20DORA%20Process%20Wireshark%20Packet%20Capture) |
| Redistribution Labs | Route redistribution across OSPF, EIGRP, RIP, and other protocol combinations | [`redistribution-labs/`](https://github.com/sheetalguragain/network-practice-labs/tree/master/Labs/Redistribution-labs) |

> More categories will be added here as new topics are practiced (e.g. VLANs/trunking, ACLs, VPNs, BGP).

## Full Lab Index

| Category | Lab | Status |
|----------|-----|--------|
| DHCP | DHCP DORA + Relay + Multi-Server (3 parts) | ⚪ Planned |
| Redistribution | Multi-Protocol Redistribution (OSPF, EIGRP, RIP) | 🟡 In Progress |

> Status legend: 🟢 Complete &nbsp;|&nbsp; 🟡 In Progress &nbsp;|&nbsp; ⚪ Planned

## Documentation Style

Every lab in this repo follows the same structure, so anyone browsing can navigate labs consistently:

```
network-practice-labs/
├── README.md                                            <- index for main repo
├── Labs/ 
    └── DHCP Dora Process Wireshark Packet Capture/
        ├──README.md                                     <- objective, topology, config, verification
        ├──WHAT-I-LEARNED.md                             <- mistake → root cause → fix → concept reinforced
        ├──configuration.md                              <- router/device running-configs
        ├──topology.png                                  <- topology diagram
        ├──verification.md                               <- verification command output
    └── Redistribution-labs/
        └── redistribution-lab-01/                       
            ├──README.md                                 <- objective, topology, config, verification
            ├──WHAT-I-LEARNED.md                         <- mistake → root cause → fix → concept reinforced
            ├──configuration.md                          <- router/device running-configs
            ├──topology.png                              <- topology diagram
            ├──verification.md                           <- verification command output
        ├── README.md                                    <- index for Redistribution-labs
    └── README.md                                        <- index for Labs Collection
```

The **WHAT-I-LEARNED.md** files are intentionally kept separate from the main lab README - they focus on real mistakes made during the lab, why they happened, and what concept each one reinforced. This is meant to be an honest learning log, not just a highlight reel of what worked.

## About Me

Networking background built through hands-on bootcamp training (CompTIA Network+, CCNA, RHCSA) completed under Jiwan Bhattarai Sir, along with real-world volunteer project experience building and maintaining websites for IT Education Nepal, Networking Nepal, and other clients.

This repo exists to keep a transparent, growing record of networking practice - labs are added here as they're completed, not staged for appearance.
