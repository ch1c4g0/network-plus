
# Data Center Interconnect (DCI)

This function allows us to seamlessly connect data centers together, segment different customer networks, and distribute applications everywhere.

Because of the different ways IP Addresses are managed across data centers, it is challenging to manage dynamically created virtual systems.

How can we seamlessly connect datacenters together without worrying about connection type, ip addressing, routing, or connectivity?

# Virtual Extensible LANs (VXLANS)

VXLAN is an overlay technology that encapsulates Layer 2 Ethernet traffic inside Layer 3 packets, commonly used to connect data center networks.

| Concept                   | Network+ meaning                                                       |
| ------------------------- | ---------------------------------------------------------------------- |
| **VXLAN**                 | Extends Layer 2 over Layer 3                                           |
| **Layer 2 encapsulation** | Wraps Ethernet frames so they can travel over an IP/routed network     |
| **Overlay**               | Virtual network built on top of the physical network                   |
| **Underlay**              | The real routed network carrying the VXLAN traffic                     |
| **DCI**                   | Data Center Interconnect; connecting data centers together             |
| **VNI**                   | VXLAN Network Identifier; similar idea to a VLAN ID, but more scalable |

**A VTEP is the VXLAN tunnel endpoint that encapsulates and decapsulates Layer 2 traffic across a Layer 3 network.**
