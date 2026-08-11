---
name: security-headers-review
description: "Read-only review of application and proxy configuration for HTTP security headers, cookie attributes, caching, framing, content-type, transport, and browser policy risks."
---

# Security Headers Review

Follow `POLICY.md`. Do not request a live URL or change server, CDN, proxy, or DNS configuration.

1. Determine which component sets or overrides headers and whether behavior differs by route, error path, environment, or cached response.
2. Review Content-Security-Policy, frame protections, HSTS, Referrer-Policy, Permissions-Policy, X-Content-Type-Options, cross-origin policies, and cache controls in context.
3. Review session and sensitive cookies for `Secure`, `HttpOnly`, appropriate `SameSite`, scope, expiry, and prefix use.
4. Flag contradictory, duplicated, obsolete, or overly permissive directives; do not treat the presence of a header as proof of safety.
5. Account for API-only routes, downloads, redirects, reverse proxies, and local development exceptions.

Report file/route evidence, affected browser boundary, impact, confidence, and a minimal configuration recommendation.

Curated from upstream `skills/performing-security-headers-audit`; active HTTP probing and scripts are excluded.
