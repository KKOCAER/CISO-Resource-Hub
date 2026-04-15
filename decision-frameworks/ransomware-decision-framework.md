# Ransomware Decision Framework

## Goal
Help leadership make fast, disciplined, and defensible choices.

## Decision Inputs
- backup integrity
- exfiltration confidence
- active spread status
- identity compromise depth
- legal and regulatory obligations
- business continuity impact

## Immediate Questions
1. can we still contain spread
2. do we trust backups
3. do we trust identity
4. what data may be exposed
5. what must be restored first

## Decision Paths

### Path A: Restore from clean state
Use when:
- spread is contained
- offline or immutable backups are valid
- identity trust can be re-established

### Path B: Delayed restore with investigation emphasis
Use when:
- threat actor persistence is unclear
- identity or management plane is still compromised

### Path C: Extreme business continuity decision
Use when:
- recovery options are materially weak
- business impact is severe
- executive and legal review is active

## Strong Default
Do not let ransom discussion replace recovery discipline.
