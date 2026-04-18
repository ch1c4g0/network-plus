
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

```
  255     .    0      .    0    .    0
11111111    11111111    11111111  00000000
            +_____________________________+
Network(24) |         Hosts(8)            |
            |_____________________________|
```
