# Zero Trust Reference Architecture

## Logical Flow

```text
User
  -> Identity Provider
  -> Device Trust Check
  -> Policy Decision
  -> ZTNA / Access Broker
  -> Application
  -> Continuous Monitoring
```

## Components
### Identity
- MFA
- SSO
- conditional access
- privileged access separation

### Device
- endpoint management
- EDR
- compliance posture
- admin workstation model

### Access
- ZTNA
- application proxy
- PAM
- session controls

### Monitoring
- SIEM
- XDR
- identity analytics
- UEBA

## Design Notes
Zero Trust works best when the application inventory and identity ownership model are clean.
