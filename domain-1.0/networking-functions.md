

<p><h1>Content Delivery Networks (CDN)</h1></p>

<p>Provides an efficient way to get data to an end-user,commonly geographically dispersed.<br>
Social Media are all CDNs.</p>

<p><h1>Virtual Private Networks (VPN's)</h1></p>

<p>A secure way to transfer data across secure or insecure networks.<br>
VPNs often use a concentrator (OpenVPN, PfSense, Site-Site VPNs ect.)</p>

<p>VPN concentrators do all the encryption and decryption, because of this VPNs often have purpose built<br>
VPN concentrators. They can run as software or hardware.</p>

<p><h1>Quality of Service (QOS)</h1></p>

<p>Often called traffic shaping or packet shaping, is the control of bandwidth / data rates on a network.<br>
Could be done within a router, switch, firewall, or QoS device.</p>

<p><h1>Time To Live (TTL)</h1></p>

<p>The defined amount of time for data to traverse the network.<br>
Could be based on time or number of hops before it is dropped.</p>

<p><h1>Routing Loops</h1></p>

<p>Each router believes the other is the next hop creating an endless cycle.<br>
TTL can be used to stop this loop.</p>

<p><h1>Internet Protocol (IP)</h1></p>

<p>IP will drop a packet after a defined number of hops, each pass through a router is a hop.<br>
Default Mac/Linux TTL is 64 hops, Default Window TTL is 128 Hops. An average amount of hops is 12 - 16 hops.</p>

<p><h1>DNS Lookups</h1></p>

<p>DNS lookups</p>

<p>TTL's within DNS Queries tells us how long to store / cache the IP for. (300 seconds = 5 minutes)</p>
