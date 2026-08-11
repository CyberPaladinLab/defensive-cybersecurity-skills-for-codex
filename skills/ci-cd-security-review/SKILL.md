---
name: ci-cd-security-review
description: "Read-only review of GitHub Actions and other CI/CD configuration for permissions, secret handling, supply-chain, and untrusted-input risks."
---

# CI/CD Security Review

## Safety boundary

Do not edit workflows, trigger jobs, change repository settings, rotate secrets, or call deployment systems.

## Review workflow

1. Inspect workflow triggers, token permissions, environment protections, secret exposure, artifact handling, cache keys, reusable workflows, and deployment gates.
2. Identify unsafe use of untrusted pull-request data in privileged contexts, command construction from event fields, excessive token permissions, write-capable jobs on untrusted code, and secret-bearing workflows that check out attacker-controlled content.
3. Review third-party actions for immutable pinning and unnecessary privileges using only the supplied workflow data and trusted current documentation when available.
4. Check whether logs, artifacts, cache contents, or environment dumps may leak sensitive values.
5. Recommend least privilege and safer trigger separation without applying changes.

## Output

Provide finding, workflow/job location, trigger conditions, privilege boundary, impact, confidence, and remediation recommendation.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/integrating-sast-into-github-actions-pipeline`
- `skills/implementing-github-advanced-security-for-code-scanning`
