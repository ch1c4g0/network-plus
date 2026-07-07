
# Infrastructure as Code (IaaC)

Managing and deploying infrastructure using code/config files instead of manually clicking through GUIs.

Defines an infrastructure (servers, network, and applications as definition files). It also allows us to implement versioning to our infrastructure similar to code versions.

```yaml
create:
  server: web01
  cpu: 2
  memory: 8GB
  network: prod-vlan
  firewall:
    allow:
      - 443
```

Infrastructure as Code uses machine-readable configuration files to automate the deployment and management of infrastructure.

| Traditional infrastructure        | Infrastructure as Code            |
| --------------------------------- | --------------------------------- |
| Click through portal/GUI          | Define resources in code          |
| Manually configure devices        | Automate deployment/configuration |
| Easy to make inconsistent changes | Repeatable and consistent         |
| Harder to track changes           | Can use Git/version control       |

**IaC = your infrastructure becomes a config file instead of a pile of manual clicks.**

## Standardization

One way to outline configuration files for continuity

## Source Control

Manages change and allows for building/publishing definiton files, ongoing changes, and versions. 

## Automation

Perfect for implementing automation to prevent configuration drift/compliance (ensures same config for all systems), provides identical deployment, seamless upgrades/changes, Dynamic Inventorying, and more.
