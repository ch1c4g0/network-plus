

# Open Shortest Path First (OSPF)

A common interior gateway protocol and used within a single autonomous system (AS)

This is a common, well-established standard, it is available on routers from many different manufacturers

## Dijkstra Algorithm or SPF

OSPF routers use *OSPF neighbors*

### OSPF Neighbors

OSPF routers form **neigbor relationships**, also called **adjacencies**

They use hello packets to discover nad maintain neighbors. For two OSPF routers to become neighbors, they need to agree upon the variables below.

| Must match        | Why it matters                                     |
| ----------------- | -------------------------------------------------- |
| Area ID           | They need to be in the same OSPF area on that link |
| Hello/dead timers | They need to agree on timing                       |
| Authentication    | If enabled, credentials must match                 |
| Network/subnet    | They need to communicate on the same link          |
| Stub area flag    | Area type must agree                               |

### OSPF Areas

OSPF areas can divide a network into segments with **Area 0 = backbone area**. All other OSPF areas connect back to Area 0.

Areas keep large OSPF networks managable with less topology info to process and routers not needing to know every detail from every area.

This makes OSPF scalable, converge faster, and a logical hierachical design.

### OSPF Advertisements

OSPF routers send LSAs to describe their links, receiving routers then store that information in the LSDB. After, SPF/Dijkstra is ran against their database to build the routing table.

### Cost Calculation 

Cost is calculated bandwidth, the higher the bandwidth, the lower the cost, making it the preferred route.

Slow link = higher cost, less preferred
Fast link = Lower cost, more preferred

### Convergence

OSPF sends updates only when topology changes, a link goes down -> router detects change -> router sends lsa -> routers update LSDB -> Routers rerun SPF -> Routing tables update. That process is convergence.

# Other notable information

- OSPFv2 -- IPv4 | OSPFv3 IPv6
- DR: Designated Router
- BDR: Backup Designated Router

# Summary

OSPF is a link-state protocol that uses the dijkstra's algorithm to calculate the lowest cost path to networks. OSPF areas limit the size of LSDB's and reduce how much topology information routers need to process, making it scalable, fast, and simple. OSPF communicates with other OSPF routers using LSA's these are then stored in LSDB's which are used in the SPF algorithm to determine the best routes, which are then added to the routing table.

