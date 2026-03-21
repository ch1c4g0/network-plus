

<p><h1>Generic Protocols and their Ports</h1></p>

<p><h1>FTP - File Transfer Protocol</h1></p>

<p>Used to transfer files between systems, it uses two ports, tcp/20 and tcp/21.<br>
TCP/20 is active mode data, tcp/21 control. 

<p><h3>TCP/21</h3></p>

**<p>Responsible for authenticating users, sending commands, and establishing the connection.</p>**

<p><h3>TCP/20</h3></p>

**<p>Responsible for transferring file data (uploading/downloading)</p>**

<p>Both of thes ports are essential for modern active FTP.</p>

<p><h1>SFTP / Secure File Transfer Protocol</h1></p>

<p>Provides encryption during file transfer using tcp/22 (secure-shell)</p>
<p>It also provides file system functionality.</p>

<p><h1>SSH / Secure Shell</h1></p>

<p>Text-based console communication on the encrypted communication link tcp/22.</p>

<p><h1>Telnet</h1></p>

<p>Out of date / insecure means of ssh, nothing is protecting whats being send back and forth.</p>

<p>SMTP / Simple Mail Transfer Protocol</p>

<p>Server to Server email transfers using tcp/25(Plaintext), or tcp/587(SMTP using TLS)</p>

<p>It is also used to send mail from a device to a mail server, other protocols are used for receiving mail (POP3/IMAP)</p>

<p><h1>DNS / Domain Name System</h1></p>

<p>Communication on UDP/53, it converts names to IP Addresses, Large transfers may use TCP/53</p>

<p>Without DNS Servers we would not be able to communicate to servers as we would not be able to find them(resolve).</p>

<p><h1>DHCP / Dynamic Host Configuration Protocol</h1></p>

<p>Allows us to automatically configure an IP address, subnet mask, and other options. DHCP operates on UDP/67 and UDP/68</p>

<p>A DHCP Server is required to accomplish this, it is typically integrated in to commerical routers.</p>

<p><h3>Dynamic / Pooled DHCP</h3></p>

<p>IP Addresses are assigned in real-time from a pool, each system is given a lease, and must renew at a set interval.</p>

<p><h3>DHCP Reservations</h3></p>

<p>Addresses are assigned by MAC Address in the DHCP Server. This provides a quick way of managing addresses from one location.</p>


<p><h1>TFTP / Trivial File Transfer Protocol</h1></p>

<p>Operates on UDP/69 for simple file transfers(no auth, not secure) typically used on VOIP.</p>

<p><h1>HTTP and HTTPs / Hypertext Transfer Protocol (Secure)</h1></p>

<p>Operates on TCP/80(unsecure) or TCP/443(Secure TLS or SSL) to interact with web applications</p>

<p><h1>NTP / Network Time Protocol</h1></p>

<p>Switches, routers, firewalls, servers, workstations all use NTP to keep clocks synced. It uses UDP/23, it is critical for systems to have correct time syncro for updates / logging and reporting.</p>

<p><h1>SNMP / Simple Network Management Protocol</h1></p>

<p>Queries devices to gather information from them, it operates on UDP/61.</p>

<p><h3>Three Versions v1, v2, and v3</h3></p>

<p>SNMP v1 allows management station to perform a single query and a single response with no encryption. SNMP v2 allows for bulk transfers and had data type ehancements for efficiency.</p>

<p>v3 is the most recent and secure version of SNMP it focuses on integrity, authentication, and encryption.</p>

<p><h3>SNMP Traps</h3></p>

<p>Sends alerts and notifications to the management center using port UDP/162</p>

<p><h1>LDAP-LDAPS / Lightweight Directory Access Protocol</h1></p>

<p>Operates on tcp/389 it is used to stored and retrieve information in a network directory.<br>

LDAPs is a secure version of LDAP(a non-standard implementation of LDAP over SSL, it uses TCP/636.</p>

