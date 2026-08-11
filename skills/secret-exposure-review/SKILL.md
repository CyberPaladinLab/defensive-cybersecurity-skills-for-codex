---
name: secret-exposure-review
description: "Read-only review for accidentally committed or logged secrets while redacting sensitive values. Use for repositories, diffs, configs, and logs."
---

# Secret Exposure Review

## Safety boundary

Do not test whether any credential is valid, contact the issuing service, access credential stores, or print full secret values. Never modify Git history or repository files.

## Review workflow

1. Inspect source, configuration, examples, tests, logs, and diffs for high-confidence secret patterns and credentials embedded in connection strings.
2. Distinguish real-looking credentials from placeholders, fixtures, documentation examples, hashes, and public identifiers.
3. Redact matched values in all output. Show only a short non-sensitive fingerprint when necessary for deduplication.
4. Check for logging paths that may expose tokens, authorization headers, cookies, private keys, database credentials, or webhook secrets.
5. Recommend rotation and secure storage when exposure appears credible, but do not perform rotation or history rewriting.

## Output

Report secret type, location, confidence, exposure path, likely scope, and remediation. Never reproduce the secret itself.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/implementing-secret-scanning-with-gitleaks`
- `skills/implementing-secrets-scanning-in-ci-cd`
