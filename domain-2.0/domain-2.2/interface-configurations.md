

# What are the variables when configuring an interface?

These configurations need to match, we can break them into two different parts Layer 2 and Layer 3 configurations

## Layer 2
- Speed: 10/100/1000/10G
- Duplex: Half/Full
- Automatic Manual

## Layer 3
- IP address
- IP subnet mask
- VLAN interfaces
- Management interfaces
- DNS

### Link Aggregation (LAG)

Port bonding, this is multiple interfaces acting like one big interface.

The main purpose is to increase available bandwidth and provide redundancy. If one physical link fails, traffic can continue using the remaining links in the group.


#### Link Aggregation Control Protocol (LACP)

**LACP** is a protocol used to automatically negotiate and manage link aggregation between network devices.

Without LACP, a LAG may need to be configured manually on both sides. With LACP, the devices can detect compatible links, form the aggregation group, and help prevent misconfiguration.

This adds additional automation and management of LAG.

| Term | Meaning |
|---|---|
| **Link Aggregation** | Combines multiple physical links into one logical link |
| **LAG** | Link Aggregation Group |
| **Port bonding / NIC teaming** | Other names for combining interfaces |
| **LACP** | Protocol that negotiates and manages link aggregation |
| **802.3ad** | IEEE standard commonly associated with LACP |

**LAG is the bundled link. LACP is the protocol that helps create/manage the bundle.**

##### Maximum Transmission Unit (MTU)

This is the largest packet/frame/payload size that can be send across the network before needing to be fragmented.
- A common MTU is 1500 bytes
    - This means a device can send up to 1500 bytes before headers at layer 2 are added.
- When a packet is too large, one of three things happen.
    - Fragmentation: Packet gets split into smaller pieces
    - Drop: The packet is discarded
    - PMTUD adjusts size: Device learns the largest safe packet size

**PMTUD: automatically determine the smallest MTU size along a data path between two hosts**

You will commonly see this when traffic is going through a process that adds extra headers like VPNs, VXLANs, PPPoE, GRE/IPsec Tunnels, or MPLS/SD-WAN.

##### Maximum Segment Size (MSS)

This is the largest amout of data in bytes that a device can receive in a single unfragmented TCP segment.
  - THIS IS ONLY COUNTING THE ACTUAL TCP PAYLOAD

#### Jumbo Frames

**INTENTIONALLY LARGE FRAMES**

Ethernet frames with more than a 1,500 byte payload
  - Up to 9,216 bytes of an MTU (9000 being normal)
  - All devices must be configured to transmit / receive jumbo frames.
  - These frames will be dropped if one of the devices does not understand them.
  - Will create "GIANT" frame error if not enabled

###### Runt and Giant Frames

Unintentionally small or large frames

1. Runt: Smaller than 64 bytes
2. Normal: 64 to 1518 (1522 bytes w/ 802.1Q VLAN tag)
3. Larger than the allowed maximum
