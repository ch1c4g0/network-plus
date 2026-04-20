
<p><h1>Classless Subnetting</h1></p>

<p>Otherwise known as CIDR (Classless Inter-Domain Routing), it was created in 1993 and removed restrictions created by classful subnet masks.</p>

<p>Subnets are expressed as decimal, bits, or CIDR notation (IP Addr, Slash, # of subnet bits); 192.168.1.44/24</p>

<p>Most computers expect the decimal based subnet mask (.255), while most routers expect CIDR notation /24.</p>

<p><h1>The subnet mask</h1></p>

<p>Contiguous series of ones, ones on the left, zeros on the right.</p>

<p>i.e</p>

```
11111111.11111111.11111111.00000000
        255.255.255.0
              /24
```

<p>There is a total of 24 ones that makeup the network portion of the subnet mask, this gives us a /24 address (8x3)</p>

<p><h1>Binary to CIDR example</h1></p>

```
11111111.11111111.00000000.00000000
```
<p>To find the CIDR-block notation we would simply change the network portion of the address to .255 and everything behind it to 0</p>

```
 255.255.0.0
```
<p>Adding the two octets of then network portion gives you 16.</p>

```
11111111.11111111.00000000.00000000
            255.255.0.0
                /16
```



<p><h2>One more example,</h2></p>

```
11111111.11111111.11111111.11000000
```

<p>255 in the place of all of your network bits, zero for all network bits, add up your network bits and thats it.</p>

```
        11111111.11111111.11111111.11000000
                255.255.255.2
                      /26
```

<p><h1>Binary to Decimal</h1></p>

```
Binary                Decimal
00000000                0
10000000                128
11000000                192
11100000                224 
11110000                240
11111000                248
11111100                252
11111110                254
11111111                255
```
<p><h2>Practice Problem</h2></p>

```
11111111.11110000.00000000.00000000
```

<p>Look at the chart above, you can recognize if there are 4 on 4 off, that is 240. 8 + 4 = /12</p>

```
255.240.0.0
```

<p><h1>CIDR to Binary/Decimal</h1></p>

<p>We can do the same conversion with the chart with just the CIDR notation as well. If we have a /20 CIDR-Block it would look like this.</p>

<p>Should be a total of 20 active bits (1s), it would look like this in Binary.</p>

````
11111111.11111111.11110000.00000000
````
<p>To get our decimal format, we would follow the same steps above.</p>

```
255.255.240.0
```
