

<p><h1>ICMP (Internet Control Message Protocol)</h1></p>

<p>The text messaging for network devices, it is it's own protocol used and carried by IP.<br>
  
This protocol allows devices to request and reply to "are you alive" requests. ICMP will tell you if your TTL Expired or if the host is unreachable.</p>

<p><h1>GRE (Generic Routing Encapsulation)</h1></p>

<p>The tunnel between two applications, this is commonly done with VPN's.</p>

><p>Encapsulates traffic within IP.</p>
>
> - Two endpoints appear to be directly connected
> - No built-in encryption (will be done separately)

<p><h1>VPNs (Virtual Private Networks)</h1></p>

<p>Encrypted (private) data traversing a public network.</p>

<p><h3>VPN Concentrators,</h3></p>

<p>Concentrators perform the encryption and decryption of VPN traffic, this service is often integrated into firewalls.</p>

<p>VPN concentrators are high-performance network devices or servers designed to securely connect remote users.</p>

<p>Acts like a VPN Gateway, authenticating users, encrypt/decrypt, and load-balancing for remote access.</p>

<p><h1>IPSec (Internet Protocol Security)</h1></p>

<p>Security for OSI Layer 3 (Network Layer), it provides authentication and encryption for every packet. It can also digitally sign each packet for integrity, this prevents replay attacks.</p>

<p>Very standardized, multi-vendor implementations are common.</p>

><p><h3>Two Core IPSec Protocols</h3></p>
>
> - <h4>Authentication Header (AH)</h4>
> - <h4>Encapsulation Security Payload(ESP)</h4>

<p><h1>Internet Key Exchange (IKE)</h1></p>

<p>Completed prior to sending data, allows both communicating parties to agree on encryption/decryption keys, this is also know as Security Association(SA).</p>

<p><h3>Phase 1</h3></p>

<p>Diffe-Hellman used to create a shared secret key using UDP/500. ISAKMP or Internet Security Association and Key Management Protocol.</p>

<p><h3>Phase 2</h3></p>

<p>Coordinates ciphers and key sizes, negotiates an inbound and outbound SA for the IPSec tunnel.</p>

![ipsec-p1-p2](https://github.com/ch1c4g0/network-plus/blob/26ed795a5022704a970cc2c812ce01c466cdd183/screenshots/Screenshot%202026-03-25%20122633.png)

<p>The first diagram in the image above shows us creating the ISAKMP Tunnel over UDP/500. The second diagram we are encluding the encrypted data via the ESP Tunnel, this is the foundation for sending data over the IPSec Tunnel.</p>

<p><h3>Transport Mode and Tunnel Mode</h3></p>

<p>You may be asked how you want to send the data, "transport", or "tunnel" both of these work differently and protect data in different ways.</p>

<p>Transport mode inserts an IPSec Header and IPsec Trailer into our information this will all be in the clear, anything within the data portion is encrypted.</p>

<p>Tunnel Mode encrypts the original IP-Header and Data. A new IP Header is added at the beggining of the data stream to instruct where to reach the IPSec concentrator. The key different between the two is the original header being encrypted and the addition of the new IP-Header to route to the concentrator.</p>

<p><h1>Encapsulation Security Protocol (ESP)</h1></p>

<p>Encrypts the packet, uses MD5, SHA-1, or SHA-2 for the hash, and 3DES or AES for encryption. It also adds a header, trailer, and an integrity check value to the IPSec datagram.</p>

````
______________________________________________________________________________________
| NEW IP Header | ESP Header | IP Header | DATA | ESP Trailer| Integrity Check Value |        
______________________________________________________________________________________

````
