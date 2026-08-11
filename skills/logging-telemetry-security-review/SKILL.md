---
name: logging-telemetry-security-review
description: "Read-only review of application logs, metrics, traces, and audit events for secret/PII leakage, injection, integrity, access, retention, correlation, and incident usefulness."
---

# Logging and Telemetry Security Review

Follow `POLICY.md`. Do not query live telemetry systems, enable logging, change retention, send test events, or upload logs.

1. Trace log, metric, trace, and audit-event creation from inputs through formatting, enrichment, transport, storage, and access.
2. Check for credentials, tokens, cookies, request bodies, personal data, cryptographic material, and overly detailed errors; redact all examples.
3. Review structured logging, untrusted-field encoding, log forging, cardinality amplification, truncation, and bounded payload handling.
4. Verify that security-relevant events capture actor, action, target, result, timestamp, and correlation identifiers without recording secrets.
5. Review integrity, access controls, retention, deletion, sampling, and failure behavior from supplied configuration only.

Report evidence location, exposure or detection gap, impact, confidence, and defensive recommendation.

Curated from upstream `skills/analyzing-api-gateway-access-logs` and the defensive logging concerns in the audited snapshot; cloud queries and scripts are excluded.
