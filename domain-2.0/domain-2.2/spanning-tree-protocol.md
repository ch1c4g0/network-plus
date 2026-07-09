

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

When a link goes down, spanning tree is able to re-calculate the Layer 2 loop-free topology and changes which switch ports are forwarding or blocking, this process is called **convergence** and typically takes 30-50 seconds. The speed of STP is a gripe, thats why **RSTP(RSTP 802.1w)** was created.

# Rapid Spanning Tree Protocol (RSTP) 802.1w

- This is a faster version of STP
- Convergence only takes a few seconds or less
- Uses alternate/backup port roles to speed recovery.

**STP and RSTP are backwards compatible**

Devices using RSTP can also use STP and so on.
