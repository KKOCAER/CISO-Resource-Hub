# CISO Resource Hub

A curated **awesome-list style** and **field-ready reference repository** for CISOs, deputy CISOs, security architects, SOC leaders, and incident commanders.

This project combines two things:

- **Curated external resources** worth reading, following, and reusing
- **Practical internal-ready content** such as playbooks, decision frameworks, templates, and reference architectures

It is opinionated toward:
- regulated enterprises
- banking and payment institutions
- telecommunications operators
- hybrid cloud environments
- crisis readiness and security leadership

---

## Why this repo exists

Most security repositories fall into one of two traps:

- they are only a long list of links
- they are only a pile of internal documents with no discoverability

This repository is designed to bridge both worlds.

You can use it to:
- **decide** which controls and investments matter
- **design** a defensible target-state architecture
- **respond** under pressure during cyber incidents
- **improve** detection, resilience, and maturity over time

---

## Repository Map

```text
CISO-Resource-Hub/
├── docs/
├── strategy/
├── awesome/
├── governance/
├── decision-frameworks/
├── architecture/
├── war-room/
├── playbooks/
├── detection/
├── use-cases/
├── industries/
├── templates/
├── metrics/
├── maturity/
├── tooling/
└── exercises/
```

---

## Start Here

### If you are a CISO
- [Strategy](strategy/)
- [Decision Frameworks](decision-frameworks/)
- [War Room](war-room/)
- [Templates](templates/)

### If you are a security architect
- [Architecture](architecture/)
- [Governance](governance/)
- [Tooling](tooling/)
- [Industries](industries/)

### If you lead SOC or IR
- [Detection](detection/)
- [Playbooks](playbooks/)
- [War Room](war-room/)
- [Exercises](exercises/)

### If you work in banking or telco
- [Industry Modules](industries/)
- [Use Cases](use-cases/)
- [Regulatory Mapping](governance/regulatory-mapping/)
- [Zero Trust](architecture/zero-trust/)

---

## Featured Content

### Crisis Leadership
- [CISO War-Room Playbook](war-room/ciso-war-room-playbook.md)
- [Ransomware War-Room Runbook](war-room/ransomware-war-room-runbook.md)
- [Data Breach War-Room Runbook](war-room/data-breach-war-room-runbook.md)

### Decision Support
- [Ransomware Decision Framework](decision-frameworks/ransomware-decision-framework.md)
- [SIEM vs XDR Decision Matrix](decision-frameworks/siem-vs-xdr-decision-matrix.md)
- [ZTNA vs VPN Decision Matrix](decision-frameworks/ztna-vs-vpn-decision-matrix.md)

### Architecture
- [Zero Trust Reference Architecture](architecture/zero-trust/zero-trust-reference-architecture.md)
- [Zero Trust Deployment Patterns](architecture/zero-trust/zero-trust-deployment-patterns.md)
- [Privileged Access Model](architecture/identity-security/privileged-access-model.md)

### Detection
- [Detection Strategy](detection/detection-strategy.md)
- [Detection Coverage Model](detection/detection-coverage-model.md)
- [MITRE Mapping Guide](detection/mitre-mapping-guide.md)

### Industry Content
- [Banking Threat Landscape](industries/banking/banking-threat-landscape.md)
- [Fraud Control Framework](industries/banking/fraud-control-framework.md)
- [Telco Threat Landscape](industries/telco/telco-threat-landscape.md)
- [Signaling Security Reference](industries/telco/signaling-security-reference.md)

---

## Awesome Lists

The `awesome/` section contains curated external references grouped by topic:

- [Awesome Frameworks and Standards](awesome/frameworks-and-standards.md)
- [Awesome Threat Intelligence](awesome/threat-intelligence.md)
- [Awesome Incident Response](awesome/incident-response.md)
- [Awesome Cloud Security](awesome/cloud-security.md)
- [Awesome AppSec](awesome/application-security.md)
- [Awesome Governance and Risk](awesome/governance-and-risk.md)

Each list favors:
- primary sources
- practical material
- stable references
- low-noise resources

---

## Build Order

If you want to extend this repository without turning it into a document dump, build in this order:

1. strategy
2. war-room
3. architecture
4. governance
5. decision-frameworks
6. detection
7. industries
8. exercises
9. awesome curation

---

## Contribution Principles

Contributions should be:
- practical
- concise
- decision-oriented
- architecture-aware
- operationally useful

Avoid:
- vendor brochure language
- generic blog-style advice
- duplicate content
- dead links
- long lists without context

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Suggested Public Positioning

This repository works best as a **public leadership-grade reference repo**:
- broad enough to be useful
- deep enough to be credible
- practical enough to be reused

A good positioning statement is:

> A curated and practical CISO reference hub for strategy, architecture, crisis leadership, detection, and industry-specific security patterns.

---

## Roadmap

- expand detection engineering examples
- add more banking and telco scenarios
- add visual architecture diagrams
- add tabletop exercise inject packs
- add board communication packs
- add vendor mapping where it improves implementation clarity

---

## License

MIT License
