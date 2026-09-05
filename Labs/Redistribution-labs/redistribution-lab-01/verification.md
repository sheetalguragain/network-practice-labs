## Verification Commands of All Devices

<h3>Show ip route of R1 Router (Redistribution Router) </h3>

```text
Gateway of last resort is not set

     17.0.0.0/30 is subnetted, 1 subnets
C       17.0.0.0 is directly connected, FastEthernet4/0
     16.0.0.0/30 is subnetted, 1 subnets
C       16.0.0.0 is directly connected, FastEthernet3/0
     2.0.0.0/32 is subnetted, 1 subnets
D       2.2.2.2 [90/156160] via 12.0.0.2, 00:09:39, FastEthernet0/0
     3.0.0.0/32 is subnetted, 1 subnets
D       3.3.3.3 [90/156160] via 13.0.0.2, 00:08:03, FastEthernet0/1
     4.0.0.0/32 is subnetted, 1 subnets
O       4.4.4.4 [110/2] via 14.0.0.2, 00:07:45, FastEthernet1/0
     5.0.0.0/32 is subnetted, 1 subnets
O       5.5.5.5 [110/2] via 15.0.0.2, 00:07:47, FastEthernet2/0
     6.0.0.0/32 is subnetted, 1 subnets
R       6.6.6.6 [120/1] via 16.0.0.2, 00:00:14, FastEthernet3/0
     12.0.0.0/30 is subnetted, 1 subnets
C       12.0.0.0 is directly connected, FastEthernet0/0
     13.0.0.0/30 is subnetted, 1 subnets
C       13.0.0.0 is directly connected, FastEthernet0/1
     14.0.0.0/30 is subnetted, 1 subnets
C       14.0.0.0 is directly connected, FastEthernet1/0
     15.0.0.0/30 is subnetted, 1 subnets
C       15.0.0.0 is directly connected, FastEthernet2/0
```
<h3>Show ip route of R2 Router (EIGRP-200) </h3>

```text
Gateway of last resort is not set

     16.0.0.0/30 is subnetted, 1 subnets
D EX    16.0.0.0 [170/261120] via 12.0.0.1, 00:10:53, FastEthernet0/0
     2.0.0.0/32 is subnetted, 1 subnets
C       2.2.2.2 is directly connected, Loopback0
     3.0.0.0/32 is subnetted, 1 subnets
D EX    3.3.3.3 [170/261120] via 12.0.0.1, 00:09:18, FastEthernet0/0
     4.0.0.0/32 is subnetted, 1 subnets
D EX    4.4.4.4 [170/261120] via 12.0.0.1, 00:09:00, FastEthernet0/0
     5.0.0.0/32 is subnetted, 1 subnets
D EX    5.5.5.5 [170/261120] via 12.0.0.1, 00:09:01, FastEthernet0/0
     6.0.0.0/32 is subnetted, 1 subnets
D EX    6.6.6.6 [170/261120] via 12.0.0.1, 00:09:14, FastEthernet0/0
     12.0.0.0/30 is subnetted, 1 subnets
C       12.0.0.0 is directly connected, FastEthernet0/0
     13.0.0.0/30 is subnetted, 1 subnets
D EX    13.0.0.0 [170/261120] via 12.0.0.1, 00:11:16, FastEthernet0/0
     14.0.0.0/30 is subnetted, 1 subnets
D EX    14.0.0.0 [170/261120] via 12.0.0.1, 00:11:16, FastEthernet0/0
     15.0.0.0/30 is subnetted, 1 subnets
D EX    15.0.0.0 [170/261120] via 12.0.0.1, 00:11:16, FastEthernet0/0
```
<h3> Show ip route of R3 Router (EIGRP-100) </h3>

```text
Gateway of last resort is not set

     16.0.0.0/30 is subnetted, 1 subnets
D EX    16.0.0.0 [170/261120] via 13.0.0.1, 00:10:25, FastEthernet0/1
     2.0.0.0/32 is subnetted, 1 subnets
D EX    2.2.2.2 [170/261120] via 13.0.0.1, 00:10:25, FastEthernet0/1
     3.0.0.0/32 is subnetted, 1 subnets
C       3.3.3.3 is directly connected, Loopback0
     4.0.0.0/32 is subnetted, 1 subnets
D EX    4.4.4.4 [170/261120] via 13.0.0.1, 00:10:06, FastEthernet0/1
     5.0.0.0/32 is subnetted, 1 subnets
D EX    5.5.5.5 [170/261120] via 13.0.0.1, 00:10:08, FastEthernet0/1
     6.0.0.0/32 is subnetted, 1 subnets
D EX    6.6.6.6 [170/261120] via 13.0.0.1, 00:10:21, FastEthernet0/1
     12.0.0.0/30 is subnetted, 1 subnets
D EX    12.0.0.0 [170/261120] via 13.0.0.1, 00:10:27, FastEthernet0/1
     13.0.0.0/30 is subnetted, 1 subnets
C       13.0.0.0 is directly connected, FastEthernet0/1
     14.0.0.0/30 is subnetted, 1 subnets
D EX    14.0.0.0 [170/261120] via 13.0.0.1, 00:10:27, FastEthernet0/1
     15.0.0.0/30 is subnetted, 1 subnets
D EX    15.0.0.0 [170/261120] via 13.0.0.1, 00:10:27, FastEthernet0/1
```
<h3> Show ip route of R4 Router (OSPF-2) </h3>

```text
Gateway of last resort is not set

     16.0.0.0/30 is subnetted, 1 subnets
O E2    16.0.0.0 [110/1] via 14.0.0.1, 00:11:22, FastEthernet1/0
     2.0.0.0/32 is subnetted, 1 subnets
O E2    2.2.2.2 [110/20] via 14.0.0.1, 00:11:22, FastEthernet1/0
     3.0.0.0/32 is subnetted, 1 subnets
O E2    3.3.3.3 [110/20] via 14.0.0.1, 00:11:22, FastEthernet1/0
     4.0.0.0/32 is subnetted, 1 subnets
C       4.4.4.4 is directly connected, Loopback0
     5.0.0.0/32 is subnetted, 1 subnets
O E2    5.5.5.5 [110/2] via 14.0.0.1, 00:11:21, FastEthernet1/0
     6.0.0.0/32 is subnetted, 1 subnets
O E2    6.6.6.6 [110/1] via 14.0.0.1, 00:11:23, FastEthernet1/0
     12.0.0.0/30 is subnetted, 1 subnets
O E2    12.0.0.0 [110/20] via 14.0.0.1, 00:11:24, FastEthernet1/0
     13.0.0.0/30 is subnetted, 1 subnets
O E2    13.0.0.0 [110/20] via 14.0.0.1, 00:11:24, FastEthernet1/0
     14.0.0.0/30 is subnetted, 1 subnets
C       14.0.0.0 is directly connected, FastEthernet1/0
     15.0.0.0/30 is subnetted, 1 subnets
O E2    15.0.0.0 [110/1] via 14.0.0.1, 00:11:24, FastEthernet1/0
```

<h3> Show ip route of R5 Router (OSPF-1) </h3>

```text
Gateway of last resort is not set

     16.0.0.0/30 is subnetted, 1 subnets
O E2    16.0.0.0 [110/1] via 15.0.0.1, 00:11:58, FastEthernet2/0
     2.0.0.0/32 is subnetted, 1 subnets
O E2    2.2.2.2 [110/20] via 15.0.0.1, 00:11:58, FastEthernet2/0
     3.0.0.0/32 is subnetted, 1 subnets
O E2    3.3.3.3 [110/20] via 15.0.0.1, 00:11:58, FastEthernet2/0
     4.0.0.0/32 is subnetted, 1 subnets
O E2    4.4.4.4 [110/2] via 15.0.0.1, 00:11:58, FastEthernet2/0
     5.0.0.0/32 is subnetted, 1 subnets
C       5.5.5.5 is directly connected, Loopback0
     6.0.0.0/32 is subnetted, 1 subnets
O E2    6.6.6.6 [110/1] via 15.0.0.1, 00:12:00, FastEthernet2/0
     12.0.0.0/30 is subnetted, 1 subnets
O E2    12.0.0.0 [110/20] via 15.0.0.1, 00:12:00, FastEthernet2/0
     13.0.0.0/30 is subnetted, 1 subnets
O E2    13.0.0.0 [110/20] via 15.0.0.1, 00:12:00, FastEthernet2/0
     14.0.0.0/30 is subnetted, 1 subnets
O E2    14.0.0.0 [110/1] via 15.0.0.1, 00:12:00, FastEthernet2/0
     15.0.0.0/30 is subnetted, 1 subnets
C       15.0.0.0 is directly connected, FastEthernet2/0
```
<h3> Show ip route of R6 Router (RIP) </h3>

```text
Gateway of last resort is not set

     16.0.0.0/30 is subnetted, 1 subnets
C       16.0.0.0 is directly connected, FastEthernet0/0
     2.0.0.0/32 is subnetted, 1 subnets
R       2.2.2.2 [120/1] via 16.0.0.1, 00:00:22, FastEthernet0/0
     3.0.0.0/32 is subnetted, 1 subnets
R       3.3.3.3 [120/1] via 16.0.0.1, 00:00:22, FastEthernet0/0
     4.0.0.0/32 is subnetted, 1 subnets
R       4.4.4.4 [120/2] via 16.0.0.1, 00:00:22, FastEthernet0/0
     5.0.0.0/32 is subnetted, 1 subnets
R       5.5.5.5 [120/2] via 16.0.0.1, 00:00:22, FastEthernet0/0
     6.0.0.0/32 is subnetted, 1 subnets
C       6.6.6.6 is directly connected, Loopback0
     12.0.0.0/30 is subnetted, 1 subnets
R       12.0.0.0 [120/1] via 16.0.0.1, 00:00:24, FastEthernet0/0
     13.0.0.0/30 is subnetted, 1 subnets
R       13.0.0.0 [120/1] via 16.0.0.1, 00:00:24, FastEthernet0/0
     14.0.0.0/30 is subnetted, 1 subnets
R       14.0.0.0 [120/2] via 16.0.0.1, 00:00:24, FastEthernet0/0
     15.0.0.0/30 is subnetted, 1 subnets
R       15.0.0.0 [120/2] via 16.0.0.1, 00:00:24, FastEthernet0/0
```
