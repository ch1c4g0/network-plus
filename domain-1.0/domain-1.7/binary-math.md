

<p><h1>Bits</h1></p>

<p>A zero or a one (off or on)</p>

<p><h1>Bytes</h1></p>

<p>Eight bits often called an octet.</p>

<p><h1>The binary to decimal conversion chart.</h1></p>

```
++++++++++++++++++++++++++++++++++++++
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
++++++++++++++++++++++++++++++++++++++
```

<p>This chart is simply multiplying the next number by 2.</p>

<p><h1>Practice Question</h1></p>

<p><h4>What is this binary in decimal,</h4></p>

```
00000010
```
<p>To do this we would simply plug the numbers into the chart above,</p>

```
++++++++++++++++++++++++++++++++++++++
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
======================================
|  0  |  0 |  0 |  0 | 0 | 0 | 1 | 0 | 
++++++++++++++++++++++++++++++++++++++
```

<p>This would make our answer 2 as we take all of our on bits and add them together.</p>

<p><h1>Another Practice Question</h1></p>

<p><h4>What is this binary in decimal,</h4></p>

```
10000010
```

```
++++++++++++++++++++++++++++++++++++++
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
======================================
|  1  |  0 |  0 |  0 | 0 | 0 | 1 | 0 |
======================================
| 128 +  0 +  0 +  0 + 0 + 0 + 2 + 0 |
++++++++++++++++++++++++++++++++++++++
```

<p>This would give us 130.</p>

<p><h1>What woud happen if we turned the entire byte on?</h1></p>

```
++++++++++++++++++++++++++++++++++++++
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
======================================
|  1  |  1 |  1 |  1 | 1 | 1 | 1 | 1 |
======================================
| 128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 |
++++++++++++++++++++++++++++++++++++++
```
<p>This would give us a total of 255, orrrr.... /24 ;)</p>


<p><h1>How to convert decimal to binary</h1></p>

<p>How many times can a given number between 1 and 255 go into the chart above.</p>

<p><h4>Example,</h4></p>

<p>Our number is 154.</p>

```
++++++++++++++++++++++++++++++++++++++
| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
======================================
|  1  |  0 |  0 |  1 | 1 | 0 | 1 | 0 |
======================================
```

> - Can 128 be subtracted from 154? Yes (ON)
> - If we add 64 to 128 is it less than or equal to 154? No (OFF)
> - If we add 32 to 128 is it less than or equal to 154? No (OFF)
> - If we add 16 to 128 is it less than or equal to 154? Yes (ON)
> - If we add 8 to 144 is it less than or equal to 154? Yes (ON)
> - If we add 4 to 152 is it less than or equal to 154? No (Off)
> - If we add 2 to 152 is it less than or equal to 154? Yes (ON)
> - If we add 1 to 154 is it less than or equal to 154? No (OFF)

<p>To get your binary number you can simply look at your chart above,</p>

<p>154 is binary is 10011010</p>

<p>The more bits you have the more possible outcomes i.e 2 bits has 4 outcomes, 3 bits has 8 and so on.</p>
