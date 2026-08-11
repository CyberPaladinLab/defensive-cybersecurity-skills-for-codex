---
name: secure-code-review
description: "Read-only defensive review of source code and diffs for actionable security bugs. Use when asked to audit code without modifying files or executing tests."
---

# Secure Code Review

## Safety boundary

Operate in read-only mode and follow the package-wide `POLICY.md`. Do not execute the application, run proof-of-concept payloads, install scanners, or change files.

## Review workflow

1. Identify trust boundaries, untrusted inputs, privileged operations, external calls, storage, serialization, authentication, and authorization paths.
2. Trace data from sources to sensitive sinks and look for missing validation, unsafe parsing, injection primitives, path traversal, insecure deserialization, request forgery, authorization gaps, race conditions, and unsafe error handling.
3. Check whether secrets, personal data, or security-sensitive state can enter logs or exceptions.
4. Review dependency and framework usage only from code and manifests available in scope; do not invent vulnerable versions or CVEs.
5. Prefer concrete, reachable bugs over stylistic concerns. Mark uncertain issues as hypotheses and state what evidence would confirm them.

## Output

For each finding provide: severity, confidence, file and line evidence, attack preconditions at a high level, impact, and a minimal defensive remediation recommendation. Do not provide offensive exploitation instructions.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/implementing-semgrep-for-custom-sast-rules`
- `skills/integrating-sast-into-github-actions-pipeline`
