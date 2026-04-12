
<p><h1>IP Address</h1></p>

<p>Every device has a unique IP Address assigned to it. IP Addresses are made up of 4 Octets/8bytes or four eight bit sections.</p>

<p><h3>Example,</h3></p>

```
192.168.1.1
```

<p>Ip addresses will also contain a subnet mask, this number usually isn't transmited across the network.<br>

It is used by the local device to determine what subnet it is on.</p>

<p><h3>Example,</h3></p>

```
255.255.255.0
```

<p><h1>Default Gateway</h1></p>

<p>This is the device that will allow you to communicate outside of your subnet. It must have an IP on your local network.</p>

<p><h1>Loopback Address</h1></p>

<p>This is an address to yourself, it ranges from 127.0.0. through 127.255.255.254</p>

<p>It serves as an easy way to self-reference, - ping 127.0.0.1</p>

<p><h1>Reserved IP Addresses</h1></p>

<p>Set aside for future use or testing, IP's 240.0.0.1 - 254.255.255.254, as well as all Class E addresses</p>

<p><h1>Virtual IP Addresses (VIP)</h1></p>

<p>Not associated with a physical network adapter, could be a virtual machine or internal router address</p>

<p>Internet Protocol Version 4</p>

<p>OSI Layer 3</p>

```
+================================================+
__|192|__     __|168|__    __|1|__      __|131|__ 
|11000000|   |10101000|   |00000001|   |100000011|
|________________________________________________|
|                |            |
  8 bits = 1 byte = 1 octet
|________________________________________________|
                      |
              32 cits = 4 bytes                    
+=================================================+
