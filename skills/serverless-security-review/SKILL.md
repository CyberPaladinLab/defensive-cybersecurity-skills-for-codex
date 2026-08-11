---
name: serverless-security-review
description: "Read-only security review of serverless functions, event triggers, IAM policies, environment variables, and data-flow boundaries."
---

# Serverless Security Review

## Safety boundary

Do not deploy, invoke, update, or reconfigure functions, cloud roles, gateways, queues, storage, or secrets.

## Review workflow

1. Inspect handlers, event sources, authorization boundaries, IAM policies, environment variables, outbound calls, storage access, retries, and dead-letter handling.
2. Check for wildcard permissions, confused-deputy paths, trusting unsigned event data, weak webhook/event verification, secret leakage, unsafe temporary-file handling, and cross-tenant data access.
3. Review concurrency and retry behavior for duplicate side effects, replay risk, and idempotency failures.
4. Distinguish template intent from actual deployed state and clearly state unknowns.
5. Recommend least privilege, explicit event verification, secret isolation, idempotency, and scoped data access.

## Output

Provide component/event source, issue, privilege or trust boundary, impact, confidence, and defensive remediation recommendation.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/performing-serverless-function-security-review`
- `skills/securing-serverless-functions`
