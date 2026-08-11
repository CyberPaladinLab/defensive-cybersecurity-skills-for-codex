---
name: oauth-scope-review
description: "Read-only review of OAuth/OIDC scopes, claims, grants, consent design, token audience, client type, and least-privilege assumptions from supplied code and configuration."
---

# OAuth Scope Review

Follow `POLICY.md`. Do not authenticate to an identity provider, enumerate tenants, use client secrets, revoke grants, or change consent settings.

1. Inventory requested scopes, resource audiences, grant types, client types, redirect boundaries, and delegated versus application permissions.
2. Compare each permission with the operation that requires it; flag wildcard, write, offline, directory-wide, or admin permissions lacking a demonstrated need.
3. Review incremental consent, token exchange, audience/issuer validation, scope-to-role mapping, tenant isolation, and confused-deputy risks.
4. Treat provider-specific scope names as context-dependent and avoid claiming risk solely from a name.
5. Recommend narrower scopes and control separation without performing revocation or configuration changes.

Report client/component, permission, evidence, excessive capability, impact, confidence, and least-privilege recommendation.

Curated from upstream `skills/performing-oauth-scope-minimization-review`; live Graph API inventory, credentials, POST calls, and remediation execution are excluded.
