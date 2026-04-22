

<p><h1>Magic Number Subnetting</h1></p>

<p>Allows us to perform the math in our head, subnetting with minimal math.<br>
Memorizing the CIDR to Decimal chart and Host Ranges will be beneficial for this.</p>

![magic](https://github.com/ch1c4g0/network-plus/blob/3d20d07505982d4fb44d5760a36d96606cdad375/screenshots/magic-number.png)

<p><h1>The Magic Number Process</h1></p>

1. Convert the subnet mask to decimal
2. Identify the interesting octet
3. Calculate the magic number (256 - the interesting octet)
4. Calculate the host range
5. Identify the network address (the first address in range)
6. Identify the broadcast address (the last address in that range)

<P><h2>Find the subnet ID of,</h2></P>

```
IP: 165.245.77.14
Subnet Mask: 255.255.240.0
```


