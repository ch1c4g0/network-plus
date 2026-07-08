

# What are routers?

Routers are like digital direction signs, every IP device has a routing table (workstations, servers, routers, etc).

The most specific route in the table is the route the router will choose.

## Route entries 

Route entries will contain multiple variables.

1. R: Route Code, correlates to the routing protocol
2. Subnet ID w/ Prefix Length i.e 10.0.0.0/24
3. Administrative Distance i.e 120
4. Metric: I.e 1
5. via
6. Next Hop: i.e 10.10.50.2
7. Route Timestamp
8. Outgoing interface

### Administrative Distances

Used by routers to determine which routing protocol has priority.

### Routing Metrics

Each routing protocol has its own way to calculate the best route

- BGP, OSPF, EIGRP

Metrics are not interchangable, the lower the metric value the better.

### First Hop Redundancy Protocol (FHRP)

Devices use a virtual IP (VIP) for the default gateway, if a router dissapears another one takes its place.

One default gateway can they become multiple redundant routers.

### Subinterfaces

A physical interface can be turned into multiple logical interfaces known as subinterfaces.

I.e trunking / multiple VLANs running over a link.

