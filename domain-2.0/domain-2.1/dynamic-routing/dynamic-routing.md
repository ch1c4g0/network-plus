

# Dynamic Routing

Routers send routes to other routers. Routing tables are updated near real-time.

## Advantages

- No manual route calculations
- New routes are populated automatically
- Very scalable

## Disadvantages

- Some overhead required (CPU, memory, bandwidth)
- Some initial configuration

Routers listen for subnet information from other routers either peer-peer or multi-cast. They also inform other routes of the information they know. They then determine the best path based on this information. When a change occurs, this process repeats.

# How do we select a routing protocol?

What is a route?
- Is it based on the state of the link?
- Is it based on distance?

How does the protocol determine best path?

How does it recover after a change?

Is it a standard or proprietary protocol?

### Routing Updates

Routing updates in dynamic environments are done differently depending on the protocol. There are two main types of routing protocols Distance-Vector and Link-State Protocols.

All the dynamic routing protocols behave differently when a network change occurs, it is important for you to know how they behave.

| Protocol  | Type                              | How updates generally work                               |
| --------- | --------------------------------- | -------------------------------------------------------- |
| **RIP**   | Distance-vector                   | Sends routing table updates to neighbors                 |
| **OSPF**  | Link-state                        | Shares link-state information and builds a topology map  |
| **EIGRP** | Advanced distance-vector / hybrid | Sends neighbor updates and calculates efficient paths    |
| **BGP**   | Path-vector                       | Shares route/path information between autonomous systems |

| Term          | Meaning                           |
| ------------- | --------------------------------- |
| **Distance**  | How far away the network is       |
| **Vector**    | Which direction/neighbor to use   |
| **Metric**    | Value used to pick the best route |
| **Hop count** | Number of routers crossed         |

Routing updates can be periodic or triggered by an event, some routing protocols are again known to use different ways of updating.

- RIP: Periodic Updates
- OSPF: event-driven, forms neighbors, exchanges link-state info, sends updates w/ topology changes.

# Convergence means all routers have updated and agree on the current network paths. faster the better.
