

# What is IPSec?

IPSec short for Internet Protocol Security, is a type of tunneling protocol that uses the IKEv2, ISAKMP, Security Policies, to negotiate secure connections. IPSec can be configured as point-to-point or mobile (remote style connection).

## IKE

IKE, short for Internet Key Exchange is responsible for negotiation and management of IKE and IPSec parameters. It authenticates secure key exchange, mutual peer authentication by shared secrets (not passwords), public keys, provides identity protection(in main mode).

### IKEv1

IKE version(1) defined in RFC 2409, uses a complex two-phase process.

#### Phase 1: Main/Aggressive Mode
> - Negotiation exchange of proposals for how to authenticate to a secure channel.
> - Selection of encryption algorithm: DES, 3DES, AES
> - Selection of authentication algorithm: MD5, SHA
> - Diffe-Hellman(DH)
> - PSKs or RSA/DSA certificates

# Main Mode

The initiator and receiver send three two-way exhanges (six total) messages to accomplish the following:
| Exchange Messages         | Purpose                            |
|---------------------------|------------------------------------|
|1 (1 and 2)| Propose and accepts encryption/authentication|
|2 (3 and 4)| Executes a DH exchange, initiator and receiver provide a psuedorandom number|
|3 (5 and 6)| Sends and verifies identities of initiator and receiver.|

Successful phase 1 negoation concludes when both ends of the tunnel agree to accept at least one set of the phase 1 parameters proposed.

#### Phase 2: Quick Mode
> - Negoation of security associations (SAs) to secure the data that traverses through the IPSec tunnel.

This requires 6-9 total messages, increasing latency.

- **Lacks native dead-peer detection mechanisms, drops tunnels during network changes**

- **Uses XAuth and symmetric authentication**

### IKEv2

IKE version (2) defined in RFC 7296, streamlines negotiation into a simple 4-message exchange (two request-response pairs) to set up both the IKE security association and IPSec security association quickly.

- **Built-in liveness checks and native support for MOBIKE(Mobility and Multihoming Protocol).**
- **allows seamless transitions(e.g., switching from Wi-Fi to Cellular) without dropping a session**
- **Supports EAP and asymmetric authentication (Certificates/PSKs)**
- **Peers cannot fall back from IKEv2 -> IKEv1**


# IKE and IPSec Relations

IKE automates the generation and negotation of keys and security associations. This provides more security for the two endpoints as manual key exchange is not needed (although supported by IPSec).

