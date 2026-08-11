---
name: privacy-data-flow-review
description: "Read-only privacy and sensitive-data flow review for data minimization, retention, access, logging, third-party sharing, deletion, and consent boundaries in application code and architecture."
---

# Privacy and Data Flow Review

Follow `POLICY.md`. Review supplied artifacts only. Do not query production data, identity providers, analytics systems, or user accounts.

1. Inventory personal, financial, credential, telemetry, and other sensitive data by source, purpose, storage, recipient, retention, and deletion path.
2. Trace identifiers across trust boundaries and identify unnecessary collection, linkability, secondary use, broad access, or unclear ownership.
3. Review consent and preference enforcement, export/deletion workflows, backup retention, analytics redaction, and third-party disclosure.
4. Check logs, metrics, traces, caches, queues, and error reports for accidental sensitive-data persistence.
5. Separate code evidence from legal conclusions; recommend specialist legal review where obligations depend on jurisdiction or contract.

Report data category, flow, evidence, privacy risk, confidence, and defensive minimization or control recommendation. Never reproduce sensitive values.

Curated from upstream `skills/performing-privacy-impact-assessment` and `skills/implementing-gdpr-data-protection-controls`; cloud DLP deployment and modification procedures are excluded.
