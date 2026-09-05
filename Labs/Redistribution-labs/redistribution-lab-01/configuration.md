## Configuration of All Routers

<h3>R1 (Redistribution Router) Configuration </h3>

 ```text
router eigrp 100
 redistribute eigrp 200 metric 10000 10 255 1 1500
 redistribute ospf 2 metric 10000 10 255 1 1500
 redistribute ospf 1 metric 10000 10 255 1 1500
 redistribute rip metric 10000 10 255 1 1500
 network 3.3.3.3 0.0.0.0
 network 13.0.0.0 0.0.0.3
 no auto-summary
```

```text
router eigrp 200
 redistribute eigrp 100 metric 10000 10 255 1 1500
 redistribute ospf 2 metric 10000 10 255 1 1500
 redistribute ospf 1 metric 10000 10 255 1 1500
 redistribute rip metric 10000 10 255 1 1500
 network 2.2.2.2 0.0.0.0
 network 12.0.0.0 0.0.0.3
 no auto-summary
```

```text
router ospf 2
 redistribute eigrp 100 subnets
 redistribute eigrp 200 subnets
 redistribute ospf 1 subnets
 redistribute rip metric 1 subnets
 network 4.4.4.4 0.0.0.0 area 0
```

```text
router ospf 1
 redistribute eigrp 100 subnets
 redistribute eigrp 200 subnets
 redistribute ospf 2 subnets
 redistribute rip metric 1 subnets
 network 5.5.5.5 0.0.0.0 area 0
 network 15.0.0.0 0.0.0.3 area 0
```

```text
router rip
 version 2
 redistribute eigrp 100 metric 1
 redistribute eigrp 200 metric 1
 redistribute ospf 2 metric 2
 redistribute ospf 1 metric 2
 network 6.0.0.0
 network 16.0.0.0
 no auto-summary
```
<h3>R2 - EIGRP 200 Configuration </h3>

```text
router eigrp 200
 network 2.2.2.2 0.0.0.0
 network 12.0.0.0 0.0.0.3
 no auto-summary
```
<h3> R3 - EIGRP 100 Configuration </h3>

```text
router eigrp 100
 network 3.3.3.3 0.0.0.0
 network 13.0.0.0 0.0.0.3
 no auto-summary
```
<h3> R4 - OSPF-2 Configuration </h3>

```text
router ospf 2
 router-id 4.4.4.4
 redistribute eigrp 200
 network 4.4.4.4 0.0.0.0 area 0
 network 14.0.0.0 0.0.0.3 area 0
```
<h3> R5 - OSPF-1 Configuration </h3>

```text
router ospf 1
 router-id 5.5.5.5
 network 5.5.5.5 0.0.0.0 area 0
 network 15.0.0.0 0.0.0.3 area 0
```
<h3> R6 - RIP Configuration </h3>

```text
router rip
 version 2
 network 6.0.0.0
 network 16.0.0.0
 no auto-summary
```
