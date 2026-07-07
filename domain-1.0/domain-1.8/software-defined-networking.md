

# SDN (Software Defined Networking)

A way to manage netowkrs using software/controller-based logic instead of individual/manual configuration

# SD-WAN (Software Defined Networking in a Wide Area Network)

A WAN for the cloud, how cloud applications communicate together.

## The Planes of SDN

Splits the functions of devices into separate logical units, extending the functioanlity and management of a single device.

- Data Plane (Infrastructure Layer)
- Control Plane (Control Layer)
- Management Plane (Application Layer)

| TERM | MEANING|
|---------------|--------------------------------------------------------------|
| Control Plane | Decides where traffic goes                                   |
| Data Plane    | Actually Forwards the traffic                                |
| SDN Controller| Central software brain that tells network devices what to do |
| APIs          | Lets apps/admin tools automate or program the network        |

### Different Processes inside each plane

- Data Plane: Processes network frames/packets, forwarding, trunking, encrypting, NAT
- Control Plane: Manages actions of the data plane, routing tables, session tables, NAT tables, dynamic routing protocol updates.
- Management Plane: Configure and manage the device, browsers, SSH, APIs


#### Related Topics

- Central Policy Management: policy defined centrally instead of logging into every device
- Zero-Touch Provisioning: Devices can be deployed with little/no manual local configuration, configs are pulled from the cloud
- Application Aware: Network makes decisions based on application needs, not just IPs/ports (i.e. Prioritize voice/video)
- Transport Agnostic: System can use different connections (broadband, LTE/5G, MPLS, fiber, ect.)

# Summary

SDN/SD-WAN are modern networking approaches that use centralized policy management, automation, APIs, application awareness, and zero-touch provisioning to simplify network management. 

| Exam keyword                  | Translation                               |
| ----------------------------- | ----------------------------------------- |
| Centralized management        | One controller/policy point               |
| Programmability               | Network can be controlled by software/API |
| Automation                    | Less manual CLI work                      |
| Control/data plane separation | Decisions separated from forwarding       |
| SD-WAN                        | SDN idea applied to WAN links             |
| Zero-touch provisioning       | Device gets config automatically          |
| Application aware             | Network reacts to app needs               |
| Transport agnostic            | Works across different WAN circuits       |
