

# Network Address Translation (NAT)

Extends the functionality of IPv4, hides internal private addresses to one external public address.

## Private IP Addresses

- Not routeable on the internet
- 10.0.0.0 - 10.255.255.255.255 (16 million addresses) Classful(A) Host_ID(24 bits) /8
- 172.16.0.0 - 172.31.255.255 (1 Million addresses Classful (B) Host_ID(20 bits) /12
- 192.168.0.0 - 192.168.255.255 (65,000 addresses) Classful (C) Host_ID(16 bits) /16

### How they're routed to the public internet.

You will send a request for an external resource, once that request hits the router it will change the IP address and forward that request on, once it receives the packet back from the destination it will perform that same translation in reverse to route that packet back to the sender. 

### NAT overload / PAT

The same thing as NAT, a randomized port number is assigned to the request and is forwarded to the router, the router will then store that address in the NAT table and match it to the converted port number.

NAT Tables are private ip addresses w/ port number -> public ip addresses w/ port number
