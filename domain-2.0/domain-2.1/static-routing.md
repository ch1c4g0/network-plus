

# How do routers route packets?

1. Identify the destination IP address by inspecting incoming packets
2. examines tables to determine the best route for that specific packet
3. Determines if the subnet is internal or external
4. if inside, forward the packet to the device
5. if outside, it is only responsible for getting it to the next hop/next router.

This set of operations is a map of forwarding locations, otherwise called a routing table.

If a router does not find a next hop inside it's routing table, it will discard that traffic.

# Static Routing

Administratively defined routes, you control it.

## Advantages

- Easy to configure/manage in smaller networks
- No overhead from routing protocols (CPU, memory, bandwidth)
- Easy to configure on "stub" networks (only one way out)
- More secure -- No routing protocols to analyze

## Disadvantages

- Difficult to administer on larger networks
- No automatic from preventing routing loops
- If a change in the network occurs, you need to manually adjust the routes
- No automatic rerouting if an outage occurs.

