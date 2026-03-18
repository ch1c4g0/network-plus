

<h1>Common Networking Equipment</h1>

<p><h1>A Router</h1></p>

<p>This is the most common device you may see or know. Given the name you can probably guess,<br>
this is an OSI Layer 3 device as it deals with routing.</p>

<p>Some switches may include a routing feature, also known as "Layer 3 Switches".<br>
The switch itself are not operating at a different OSI Layer, it just has both features within one device.</p>

<p>It often connects diverse network types (LAN, WAN, Copper, Fiber)</p>

<p><h1>A Switch</h1></p>

<p>These devices forward traffic based on the data link address. It is done within the hardware<br>
called ASIC or Aplication-Specific Integrated Circuit.</p>

<p>These devices may provide power over ethernet / POE.</p>

<p><h1>Firewalls</h1></p>

<p>Allows you to filter traffic based on port number or applications.<br>
There are two different types, Traditional, or NGFW.</p>

<p>Allows you to encrypt traffic (site-site VPN's)</p>

<p>Most firewalls can also perform routing functions(layer 3), often sitting on the<br>
Ingress of Egress points</p>

<p>Many firewalls also support NAT (Network Address Translation) aswell as Dynamic Routing.</p>

<p><h1>IDS and IPS</h1></p>

<p>Intrusion Detection and Intrusion Prevention can be standalone devices that either passively<br>
or actively monitor threats and may prevent them. Detection = Alert Prevention = Stop</p>

<p><h1>Load Balancers</h1></p>

<p>These devices distribute load across multiple devices to keep critical systems online.<br>
They are invisible to end-users and provide Fault Tolerance(Server outages have no effect, quick convergence)</p>

![load-balancer](https://github.com/ch1c4g0/network-plus/blob/2a002f1db5fd842e25d8c5296e6d6394921fd05a/screenshots/Screenshot%202026-03-18%20133914.png)

<p>Can provide a configurable load managed across all servers, TCP Offload, SSL Offload<br>
Decryption/Encryption, Caching, Prioritization, and Content Switching.</p>

<p><h1>Proxies</h1></p>

<p>Sits between the users and external network, it receives a users request<br>
and performs the request on their behalf.</p>

<p>This is extremely useful for caching information such as access control, URL filtering,<br>
and content scanning.</p>
