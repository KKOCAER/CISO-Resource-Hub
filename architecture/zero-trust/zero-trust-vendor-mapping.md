# Zero Trust Vendor Mapping

This file is intentionally vendor-aware but not vendor-dependent.

## Example Capability Mapping
| Capability | Common Implementations |
|---|---|
| Identity provider | Microsoft Entra ID, Okta |
| Device trust | Microsoft Intune, Jamf, endpoint posture tooling |
| EDR | Microsoft Defender, CrowdStrike, SentinelOne |
| ZTNA | Zscaler, Netskope, Palo Alto Prisma Access, Cloudflare |
| SIEM | Microsoft Sentinel, Splunk, Elastic |

## Principle
Map products to capabilities only after the target-state access model is defined.
