# Ransomware War-Room Runbook

## Trigger
Evidence of encryption, widespread file renames, extortion note presence, or confirmed ransomware behavior.

## Goals
- stop spread
- protect backups
- preserve evidence
- restore safely

## Immediate Actions
- isolate affected endpoints and servers
- restrict lateral movement protocols where feasible
- disable clearly compromised identities
- protect backup systems and backup credentials
- validate if management plane is trustworthy

## Decision Points
- do we trust the identity plane
- do we trust backups
- is exfiltration likely
- can the environment be segmented cleanly

## Recovery Rules
- rebuild trust before reconnecting broadly
- restore in business-priority order
- monitor aggressively for reinfection
