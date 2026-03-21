

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



