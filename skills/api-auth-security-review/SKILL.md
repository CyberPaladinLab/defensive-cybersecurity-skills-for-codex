---
name: api-auth-security-review
description: "Read-only review of API authentication, authorization, session, token, webhook, and key-handling logic without bypass testing."
---

# API Authentication and Authorization Review

## Safety boundary

Do not attempt authentication bypass, brute force, token forgery, credential validation, or live endpoint probing.

## Review workflow

1. Trace how identities, API keys, sessions, tokens, scopes, roles, and ownership checks are created and verified.
2. Check for missing object-level authorization, inconsistent permission checks, trusting client-supplied identity fields, insecure token storage, overly long token lifetimes, missing audience/issuer validation, and weak webhook verification.
3. Review replay resistance, nonce/timestamp handling, rate-limit assumptions, revocation paths, and separation between public and privileged operations.
4. Inspect error and logging behavior for credential or authorization leakage.
5. Recommend least privilege, centralized authorization, explicit verification, and safer secret handling.

## Output

Provide code path, boundary being enforced, weakness, preconditions at a high level, impact, confidence, and remediation. Do not generate bypass payloads.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/implementing-api-key-security-controls`
- `skills/testing-jwt-token-security`
