---
name: supply-chain-provenance-review
description: "Read-only review of build provenance, artifact signing, attestations, source pinning, release boundaries, and verification policy using supplied repository and metadata artifacts."
---

# Supply-chain Provenance Review

Follow `POLICY.md`. Do not sign, push, download, install, build, publish, or verify against a live transparency service.

1. Map source revision, builder identity, build inputs, dependencies, artifact digests, attestations, signatures, release promotion, and verification gates.
2. Check whether mutable tags, branches, registries, actions, modules, or installers can change without review.
3. Review the supplied provenance statement for subject digest, predicate type, builder, invocation parameters, materials, timestamps, and trust-root assumptions.
4. Identify gaps between producing an attestation and actually enforcing it at consumption/deployment.
5. Recommend immutable references, isolated builds, scoped signing identities, protected releases, and explicit verification policy.

Report artifact or workflow evidence, broken trust assumption, impact, confidence, and defensive recommendation.

Curated from upstream `skills/implementing-supply-chain-security-with-in-toto` and `skills/implementing-github-advanced-security-for-code-scanning`; signing, upload, installation, and workflow modification are excluded.
