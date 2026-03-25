

<p><h1>Benefits of the Cloud</h1></p>

> - On-demand compute power
> - Elasticity(Scale up or down as needed)
> - Applications can also scale
> - Access from anywhere
> - Multitenancy (Many different clients are using the same infrastructure)

<p><h1>Virtual Networks</h1></p>

<p>Virtualization of our architecture.<br>
This may be servers, firewalls, or other networking devices.</p>

<p><h1>Network Function Virtualization (NFV)</h1></p>

<p>Replaces physical networking devices and managed from a hypervisor.<br>
The function is the same as a physical device and are quickly deployed.</p>

><p>There are many different options for deployment such as,</p>
>
> - Virtual Machine
> - Container
> - Fault Tolerance
> - Ect.

<p><h1>Connecting to the cloud</h1></p>

<p><h3>Virtual Private Clouds (VPC)</h3></p>

<p>A pool of resources created in a public cloud.<br>
It is common to create many VPCs. VPCs are connect with a transit gateway kinda like a cloud router.</p>

<p>VPCs are commonly on different IP Subnets connects are often through a site-site VPN.</p>

<p>Allowing users access can be done through a VPCG(Virtual Private Cloud Gateway)</p>

<p><h3>Virtual Private Cloud Gateways</h3></p>

<p>Network Address Translation, private cloud subnets connect external resources but those external resources cannot access the private cloud.</p>

<p>Traffic to all of these objects can be limited with security groups and lists.<br>
This may be done through a cloud firewall, Layer 4 portnumbers (TCP and UDP), and Layer 3 Addresses.</p>

<p><h3>Network Security Groups</h3></p>

<p>Assign a security rule to a specific VNIC applying those controls to only specified devices.</
                                                                                                 
**<p>NOTE: VNICS are Virtual Network Interface Cards.</p>**
