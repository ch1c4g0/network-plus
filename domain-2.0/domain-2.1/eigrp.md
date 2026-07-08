

# Enhanced Interior Gateway Routing Protocl (EIGRP)

Partly proprietary to Cisco, most commonly used on Cisco routed networks. It is realtively easy to use.

*Topology changes are fast and clean, bandwidth usage is efficient.*

This protocol is a hybrid protocol as it uses both distance-vector and link-state protocols. Rather than sending its entire routin table regularly, EIGRP exchanges partial, incremental updates only when a change occurs.

## Tables used to Operate

1. Neighbor Table: Stores information about directly connected EIGRP routers that share a common data link.
2. Topology Table: Contains all routes learned from neighbor routers, tracking all possible paths to a destination.
3. Routing Table: The absolute best or successor routes actively used to forward traffic.

### Operates at Layer 3 (Network Layer)

This means EIGRP does NOT have a port number, as it does not operate at the transport layer like typical protocols.

It is identified by an IP protocol number of 88 within the IP packet header or the next header 88 for IPv6.
