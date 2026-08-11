---
name: threat-modeling-readonly
description: "Read-only threat modeling of a codebase or architecture using trust boundaries, assets, entry points, and abuse cases without active testing."
---

# Read-only Threat Modeling

## Safety boundary

Model risks only from authorized architecture, code, configuration, and documentation. Do not probe systems or generate operational offensive procedures.

## Workflow

1. Identify assets, identities, trust boundaries, data stores, external dependencies, privileged components, and security objectives.
2. Map entry points and data flows, then enumerate plausible abuse cases around spoofing, tampering, repudiation, information disclosure, denial of service, and privilege boundary failures.
3. Prioritize by realistic preconditions, blast radius, detectability, and business impact.
4. Note existing controls and residual risk. Avoid treating framework mappings as proof that a vulnerability exists.
5. Produce mitigations at architecture and control level, with validation ideas that remain read-only.

## Output

Provide a concise threat model with assets, trust boundaries, top threats, affected components, existing controls, gaps, recommended mitigations, and confidence/assumptions.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/implementing-threat-modeling-with-mitre-attack`
- `skills/performing-threat-modeling-with-owasp-threat-dragon`
- `skills/conducting-cyber-risk-assessment-with-nist-800-30`
