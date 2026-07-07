

# The Problem

There are an estimated 20 Billion devices connected to the internet, IPv4 only support 4.29 Billion. The address space for IPv4 is exhausted.

## Network Address Translation

NAT is a work-around for IPv4 Exhaustion. It maps internal IP Addresses (Private) to one external IP Address (Public), this also provides security for internal devices.

Although NAT works well in most cases, it can be a challenge with certain protocols, this is where IPv6 comes in.

# IPv6 Addressing

These addresses use a 128-bit(16 bytes) prefix compared to the 32bit prefix of IPv4 addresses. You and I will probably never ever have to worry about running out of IPv6 addresses.

IPv6 addresses are represented in Hexadecimal separated by colons.

```
fe80::5d18:652:cffd:8f52
```

## IPv6 Compression

This helps shorten the incredibly long format of IPv6 addresses. It's easier to show visually,

```
2600:DDDD:1111:0001:0000:0000:0000:0001
```

1. Remove leading Zeros

```
2600:DDDD:1111:    1:    0:    0:    0:    1
```

2. Abbreviate Groups of zeros with double colons

```
2600:DDDD:1111:    1::                      1
```

**This would leave us with a final format of: 2600:DDDD:1111:1::1**

### Communicating between IPv4 and IPv6

Not all devices can talk IPv6 such as legacy devices, embedded systems, and more. 

To perform this communication we can use tunnels to encapsulate one protocol within another, dual-stack or having the option of using both, ot translating one version to another.

These are all short-term solutions to a long-term goal of full IPv6 migration.

### Known Solutions

#### 6to4 Addressing *UNCOMMON*

Sends IPv6 over IPv4 by creating an IPv6 Address based off an IPv4 address, requiring a special relay router, and no NAT support.

#### 4in6 Tunneling *UNCOMMON*

Tunneling IPv4 traffic on IPv6 networks.

#### Dual-stack routing

Run both IPv4 and IPv6 at the same time, interfaces will be assigned multiple address types. Two separate routing tables will be maintained and separated, as well as IPv4/6 specific dynamic routing protocols.

#### Translating between IPv4 and IPv6

Done through NAT (NAT64) translate between IPv4-6 seamlessly to the end user.

We need a NAT64-capable router to translate as IPv6 is not backwards compatible, as well as a DNS64 server to translate the DNS requests.

*In order to communicate between v4/v6 you NEED a DNS64 Server and NAT64 Router*
