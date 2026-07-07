
# Zero Trust

A holistic approach to network security. It covers every device, process, and person.

Nothing is inherently trusted: MFA, Encryption, System Permissions, Firewalls, Monitoring, Analytics, etc.

## Policy-based authentication

- Adaptive Identity: Considers the source and requested resources
    - Mulitple Risk Indicators: Relationship to organization, location, type of connection, IP Address, etc.
    - Authentication can be made stronger if needed.

## Policy-driven access control

Combine the adaptive identity with a predefined set of rules. Each decision is then evaluated based on policy and a condition is set (Grant, Deny, Revoke)

## Authorization

Now that authentication is completed, this determines what applications/data are accessible to the authenticated user. These rights will vary depending on the user. To determine authorization, we should use the principle of least privileg.

### Least Privilege Access

The concept that rights and permissions should be the bare minimum needed to complete your objective. All user accounts, application accounts, and administrator accounts should follow this prephase. This limits the scope of malicious behaviors.
