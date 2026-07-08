
# Virtual Local Area Network (VLAN)

Logical separation (segmentation) of subnets in a network into separate broadcast domains.

Say you have a switch with 8 interfaces, you can have 8 separate networks with VLANs.

- There are a maximum of 4094 possible VLANS
- 0 - 1005 are normal VLANs
- 1006 - 4094 are extended VLANs
- 0 and 4095 are reserved VLAN numbers
- Native VLANs do NOT tag trunked connections
    - Native VLANs need to match between two different devices.

## How do we connect VLANs across switches?

**802.1Q Trunks**
- All VLANs on a switch are routed through the trunk.
- It does this by inserting a VLAN tag into the ethernet frame

**Normal Ethernet Frame**

|          |     |                 |            |      |         |     |                                                        
|----------|-----|-----------------|------------|------|---------|-----|
| Preamble | SFD | Destination MAC | Source MAC | Type | Payload | FCS |

**802.1Q Tagged Frame**

|          |     |                 |            |      |      |         |     |                                                     
|----------|-----|-----------------|------------|------|------|---------|-----|
| Preamble | SFD | Destination MAC | Source MAC | VLAN | Type | Payload | FCS |

