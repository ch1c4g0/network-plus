

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

<p><h3>Important Rules,</h3></p>

1. If the mask is 255, copy the IP address to the subnet ID.
2. If the mask is Zero, copy the zero to the subnet ID.
3. If not 255 or 0, this is your interesting octet.

<p><h3>Using the interesting octet to calculate subnet ID for that column,</h3></p>

1. Subtract the interesting octet subnet mask from 256 this is your magic number (available hosts per subnet).
2. Look at IP Address and fit it between a range of 0-240, and add that number into the subnet ID.

<p><h3>Calculating the broadcast address,</h3></p>

1. If mask = 255 copy to broadcast address
2. If mask = 0 fill value with 255
3. If not 255/0 interesting octet
4. Subnet ID + Magic Number - 1 =  Interesting Octet.

<p><h3>Finding Host Range,</h3></p>

1. First host = Subnet ID + 1 i.e (165.245.64.0 = 165.245.64.1)
2. Last Host = Broadcast - 1 i.e (165.245.79.255 = 165.245.79.254)

