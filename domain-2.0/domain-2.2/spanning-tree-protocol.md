

# Spanning Tree Protocol (STP) -- IEE Standard 802.1D

This protocol is how we prevent layer 2 loops when connecting multiple switches together.

Without it, layer 2 loops can easily bring down a network.

## Spanning Tree Port States

1. Blocking: Not forwarding -- loop prevention
2. Listening: Not forwarding and cleaning the MAC table
3. Learning: Not forwarding and adding to the MAC table
4. Forwarding: Data passes through and is fully operational
5. Disabled: Administratively disabled (turned off on purpose)

## Spanning Tree Ports

1. Root Ports: Connected to the designated root bridge
2. Designated Ports: Any other port that can forward traffic
3. Blocked Ports: Ports that spanning tree has disabled from sending/receiving traffic. (loop prevention)

