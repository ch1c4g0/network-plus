

<p><h1>Why do we calculate subnets?</h1></p>

<p>It would be impossible for one device to know where every other device may be. Routers are responsible for understanding how to reach a target machine.</p>


<p><h1>How do we create smaller networks?</h1></p>

<p><h2>VLSM (Variable Length Subnet Mask)</h2></p>

<P>Removes inefficiencies with class-based subnetting, it allows network administrators to define the subnet mask to specific network requirements.</P>

<p>10.0.0.0/8 is the Class A subnet, 10.0.1.0/24 and 10.0.8.0/26 would be VLSM.</p>

<p><h2>Defining Subnets</h2></p>

<p>Number of subnets = 2^of subnet bits,<br>
Hosts per subnet = 2^host bits - 2</p>

```
IP: 10..1.1.0
-- Class A, mask of 255.0.0.0
-- Classful addressing
          Network(8)  Subnet Bits (16) Host (8)
In binary, 11111111.11111111.11111111.00000000
```
<p>2 to the power of 16(subnet bits) is 65,536 total subnets<br>
2 to the power of 8(host bits) - 2 is 254, the total number of hosts per subnet. </p>

<p><h2>Another example,</h2></p>

```
IP: 192.168.11.0/26
-- Class B, mask of 

