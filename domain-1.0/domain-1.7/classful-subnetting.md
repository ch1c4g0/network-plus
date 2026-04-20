
<p><h1>Classful Subnetting</h1></p>

<p>A method of describing an IP address as it relates to it's subnet mask. Although not used today, it is still references in casual conversations.</p>

<p><h1>The Classes</h1></p>

<P><h2>Class A</h2></P>

```
  255     .    0      .    0    .    0
11111111    00000000    00000000  00000000
            +_____________________________+
Network(8)  |         Hosts(24)           |
            |_____________________________|
```

<p><h2>Class B</h2></p>

```
  255     .    0      .    0    .    0
11111111    11111111    00000000  00000000
            +_____________________________+
Network(16) |         Hosts(16)           |
            |_____________________________|
```

<p><h2>Class C</h2></p>

```
  255     .    0      .    0    .    0
11111111    11111111    11111111  00000000
            +_____________________________+
Network(24) |         Hosts(8)            |
            |_____________________________|
```

<p><h1>All of the Classes</h1></p>

<p>Below shows all addresses (0-255) and what class they belong to. Class D and E belong to a reserved block with an unspecified subnet mask.</p>

![subnetting classes](https://github.com/ch1c4g0/network-plus/blob/9b4458cffed4666c4aec2834307479cac2961094/screenshots/subnetting.png)

<p><h1>4 Values for Subnet Construction</h1></p>

<p><h2>(1.)Network Addresses</h2></p>

<p>The first IP Address of a subnet, set all host bits to 0.</p>

<p><h2>(2.)The first useable host address</h2></p>

<p>One number higher than the network address.</p>

<p><h2>(3.)Network broadcast address</h2></p>

<p>The last IP Address of a subnet, set all host bits to 1 (255 decimal)</p>

<p><h2>(4.)Last useable host address</h2></p>

<p>One number lower than the broadcast address</p>

<p><h1>Practice Your Subnet Calculations</h1></p>.

```
10.74.22.11
```

> - Class A Address
> - Subnet mask of 255.0.0.0
> - Network Address 10.0.0.0
> - First Host Address 10.0.0.1
> - Broadcast Address 10.255.255.255
> - Last Useable 10.255.255.254

```
172.16.88.200
```

> - Class B
> - Subnet mask of 255.255.0.0
> - Network Address 172.0.0.0
> - First host address 172.0.0.1
> - Broadcast address 172.255.255.255
> - Last useable address 172.255.255.254

```
192.168.4.77
```

> - Class C
> - Subnet mask 255.255.255.0
> - Network address 192.168.4.0
> - First host address 192.168.4.1
> - Broadcast address 192.168.4.255
> - Last useable address 192.168.4.254
