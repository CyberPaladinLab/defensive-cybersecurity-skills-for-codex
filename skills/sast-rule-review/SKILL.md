---
name: sast-rule-review
description: "Read-only review and design of repository-local SAST rules, including source/sink modeling, sanitizers, reachability, false positives, and safe test fixtures, without running scanners."
---

# SAST Rule Review

Follow `POLICY.md`. Do not install or execute a scanner, download registry rules, upload code, or edit repository files.

1. Define the security property, affected languages/frameworks, untrusted sources, sensitive sinks, and valid sanitizers.
2. Prefer semantic or taint-aware matching when simple text patterns would be noisy.
3. Check rule scope, exclusions, metavariable constraints, generated/vendor code handling, and likely bypasses caused by incomplete syntax coverage.
4. Design inert local fixtures with positive and negative cases; do not include live secrets or executable attack payloads.
5. Review supplied findings against reachable code before recommending enforcement severity.

Output the proposed rule logic or a patch suggestion as text only when requested, plus assumptions, false-positive risks, and safe validation guidance.

Curated from upstream `skills/implementing-semgrep-for-custom-sast-rules`; installation, scanner execution, CI writes, and upstream scripts are excluded.
