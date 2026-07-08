

# Border Gateway Protocol (BGP)

BGP is a exterior dynamic routing protocol used to route mutliple **Autonomous Systems (AS)**. This protocol is mainly used between organizations/ISPs, typically not in a normal LAN.

BGP is a path-vector routing protocol, this means it chooses path based on path information and attributes, not just hop count or cost.

BGP uses TCP port 179.

## Two different BGP Types

1. eBGP: External BGP; this is BGP used between different autonomous systems
2. iBGP: Internal BGP; this is BGP within the same autonomous system.

### BGP path metric attributes

Uses path attributes and ASNs.

**ASN = Autonomous System Number** it identifies a network to BGP and assists in the routing selection process.

1. AS PATH: List of autonomous systems a route passes through
2. Next Hop: Next router to reac the destination
3. Local Preference: Preferred outbound path inside an AS
4. MED: Suggests preferred inbound path to another AS

**BGP IS NOT DESIGNED TO BE THE FASTEST CONVERGING PROTOCOL, IT'S DESIGNED TO BE SCALABLE AND POLICY-DRIVEN.**

# Summary

BGP is a path-vector exterior gateway protocol that exchanges routing information between autonomous systems and is commonly used for Internet routing and multi-homed ISP connections.
