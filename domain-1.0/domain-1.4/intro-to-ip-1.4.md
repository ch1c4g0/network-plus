

<p><h1>Packet Life Analysis</h1></p>

<p>First important question we need to ask is what are we attempting to accomplish?</p>

<p>When it comes to networking, we are attempting to move large amounts of data efficiently.</p>

<p><h3>We can use the analogy of a moving van,</h3></p>

> - Network Topology is the Road (Ethernet, DSL, Cables)
> - The truck is the IP (Internet Protocol)
> - Boxes in your the truck are TCP and UDP
> - Inside the boxes provides more information (Application Info)

<p><h1>Breaking down IP</h1></p>

**<p>Client-Server Relationship</p>**

<p>An ethernet packet contains the ethernet header, payload, and trailer</p>

<p>Inside the payload you'll have IP information, TCP/UDP headers, and the TCP/IP Payload. Right before our trailer you'll have your HTTP Data.</p>

<p><h1>TCP and UDP</h1></p>

<p>Transported inside of IP, encapsulated by the IP Protocol. TCP and UPD operate at OSI Layer 4.</p>

<p><h3>Multiplexing</h3></p>

<p>Part of TCP/IP, it defines the ability to transmit many different applications to many different devices at the same time.</p>

<p><h1>TCP / Transmission Control Protocol</h1></p>

<p>Connection oriented, formal connection setup and close. It prioritizes reliable delivery as well as being able to recover from errors.</p>

<p>TCP also has the ability to manage out-of-order messages/retransmissions, and flow control meaning the receiver can control how much data is sent.</p>

<p><h1>UDP / Userdatagram Protocol</h1></p>

<p>Connectionless, no formal open or close / session. It prioritizes delivery over reliability/integrity, it just wants the data to arrive to its target.</p>

<p><h1>IPv4 Sockets</h1></p>

<p>Contain the following data.</p>

<p>Server IP Address, Protocol, Server Application Port Number, Client IP Address, Protocol, Client Port Number.</p>

<p><H1>Non Ephemeral Ports</H1></p>

<p>Permanent Port Numbers, Ports 0 - 1023.</p>

<p><h1>Ephemeral Ports</h1></p>

<p>Temporary port numbers, ports 1024 - 65.535</p>

<p><h1>Port Numbers</h1></p>

<p>Ranges between 0 and 65,535 with most services using non-ephemeral(not-temporary) ports.</p>

<p>Port Numbers are just for transportation not security. TCP and UDP port numbers are different(i.e tcp -p 80, and udp -p 80)</p>


