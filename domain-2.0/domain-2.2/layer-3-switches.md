
# What are layer 3 switches?

A layer 2 switch with layer 3 capabilities.

This allows us to route between VLANs without another switch, these are called SVI's.

## Switched Virtual Interfaces (SVIs)

An SVI is a virtual interface on a switch that provides Layer 3 routing for a VLAN.

Think of this as the default gateway IP for a VLAN on a layer 3 switch.

Without routing VLAN 10 and VLAN 20 are separate layer 2 networks and cannot directly talk.

With SVIs it would look like this

```
VLAN 10 SVI: 192.168.10.1
VLAN 20 SVI: 192.168.20.1
```

# EXAM CLUES:

| Clue                                  | Answer |
| ------------------------------------- | ------ |
| “Virtual interface for a VLAN”        | SVI    |
| “Default gateway on a Layer 3 switch” | SVI    |
| “Used for inter-VLAN routing”         | SVI    |
| “interface vlan 10”                   | SVI    |




