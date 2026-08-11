---
name: iac-security-review
description: "Read-only review of Terraform, CloudFormation, Kubernetes, Helm, and related infrastructure-as-code for identity, network, storage, encryption, exposure, and state-management risks."
---

# Infrastructure-as-Code Security Review

Follow `POLICY.md`. Do not initialize providers, render charts with untrusted plugins, run plans, contact cloud APIs, or apply changes.

1. Map resources, trust relationships, identities, public entry points, sensitive stores, encryption controls, and cross-account/project boundaries.
2. Review wildcard permissions, public access, broad trust principals, insecure defaults, plaintext secrets, mutable artifacts, and missing protection controls.
3. Check remote-state configuration, provider/module source pinning, integrity constraints, variable defaults, outputs, and generated artifacts.
4. Account for modules and environment overlays; do not infer deployed state from templates alone.
5. Prioritize reachable high-impact misconfigurations over generic compliance observations.

Report resource and file location, risk, realistic consequence, confidence, and defensive remediation as a recommendation only.

Curated from upstream `skills/implementing-infrastructure-as-code-security-scanning`; scanner execution, CI modification, installers, and scripts are excluded.
