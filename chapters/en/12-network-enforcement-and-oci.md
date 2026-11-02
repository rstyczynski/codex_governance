## 12. Network Enforcement and OCI Network Firewall

The gateway can enforce policy only for traffic that reaches it. The proposed network layer therefore restricts direct access from managed devices and workloads while permitting the gateway's approved upstream connections. DNS, HTTP proxy and firewall rules have complementary roles, and none should be treated as a complete solution on its own.

**Chapter sketch**

| Layer | Proposed role | Boundary to verify |
| --- | --- | --- |
| Managed DNS | Restrict unapproved names and resolution paths | Does not inspect prompts or distinguish accounts on one service |
| HTTP proxy / Secure Web Gateway | Control supported web traffic and apply inspection | HTTPS inspection requires managed trust and compatible clients |
| Network firewall | Enforce permitted routes and outbound destinations | Only covers traffic routed through the enforcement point |
| Endpoint management | Maintain controls away from the office | Requires managed devices and restrictions on bypass mechanisms |

- Inventory IPv4, IPv6, alternate DNS, encrypted DNS, tunnels and off-network access.
- Separate model inference from authentication and other required connections; avoid a blanket block that makes an approved client unusable.
- Assess client certificates, TLS inspection compatibility and unsupported protocols without weakening certificate validation.
- Route OCI workload traffic and, where designed, company-network traffic through the enforcement point.
- Require endpoint or remote-access controls for employee devices; an OCI firewall alone does not cover arbitrary laptop connections.

OCI Network Firewall is Oracle's managed network firewall powered by Palo Alto Networks. Oracle documents address and URL filtering, intrusion detection/prevention and TLS inspection. These features do not establish that the managed OCI service includes the separate Palo Alto Enterprise DLP or AI Access Security products. [Oracle service overview](https://docs.oracle.com/en-us/iaas/Content/network-firewall/overview.htm). A Secure Web Gateway implementation illustrates the additional traffic-routing and certificate requirements of HTTPS inspection. [HTTP filtering documentation](https://developers.cloudflare.com/cloudflare-one/traffic-controls/get-started/http/).

**Planned output:** An egress policy, routing diagram, exception list and bypass-test results.

