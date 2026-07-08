
# Routing Information Protocol (RIP)

RIP is a distance-vector routing protocol that uses hop count as its metric.

RIP allows routers to share routes with neighbors automatically. Instead of manually adding static routes, routers using RIP say "Here are then networks I know, they are x amount of hops away"

## Important information 

- 15-hop maximum, 16 is unreachable
- RIP only cares about hop count, the less hops will be the preferred route.
- RIP broadcasts it's entire routing table every 30 seconds
- RIPv1 and RIPv2 do flash updates, which are partial updates only accounting for changes.
- RIPv1 = Classful (A,B,C)
- RIPv2 = Classless, supports VLSM/CIDR


### RIP Versions

| Version   | Meaning                                          |
| --------- | ------------------------------------------------ |
| **RIPv1** | Classful; does not support VLSM/CIDR well        |
| **RIPv2** | Classless; supports VLSM/CIDR and authentication |
| **RIPng** | RIP for IPv6                                     |
