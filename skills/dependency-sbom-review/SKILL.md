---
name: dependency-sbom-review
description: "Read-only review of supplied CycloneDX or SPDX SBOMs for component identity, version, provenance, license, transitive-path, completeness, and vulnerability-correlation quality."
---

# Dependency and SBOM Review

Follow `POLICY.md`. Do not generate an SBOM by running build tools, query vulnerability APIs, install scanners, or upload an SBOM.

1. Validate format, component identifiers, versions, package URLs, hashes, dependency edges, scope, and metadata describing how the SBOM was produced.
2. Compare the supplied SBOM with local manifests and lockfiles when available; identify missing, duplicate, unresolved, or unexpectedly bundled components.
3. Treat vulnerability records as claims requiring a matching resolved component/version and trustworthy advisory evidence.
4. Trace transitive paths and distinguish runtime, development, optional, vendored, and unreachable components.
5. Review licenses and provenance as engineering risks without making definitive legal conclusions.

Report component, evidence, dependency path, confidence, impact, and defensive recommendation. Clearly mark stale or unverifiable advisory data.

Curated from upstream `skills/analyzing-sbom-for-supply-chain-vulnerabilities`; NVD calls, tool installation, and source scripts are excluded.
