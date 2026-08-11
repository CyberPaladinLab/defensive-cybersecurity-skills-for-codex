---
name: dependency-risk-review
description: "Read-only review of dependency manifests and lockfiles for supply-chain and dependency-management risks without installing or contacting external scanners."
---

# Dependency Risk Review

## Safety boundary

Do not install packages, execute package scripts, download artifacts, or query external package services unless a separate trusted read-only documentation tool is explicitly authorized by the user.

## Review workflow

1. Inspect manifests, lockfiles, hashes, package sources, Git dependencies, local path dependencies, and version constraints.
2. Flag unpinned or unexpectedly broad dependencies, direct URL installs, mutable Git references, unexpected registries, lifecycle-script risk, typosquatting indicators, and missing lockfiles where reproducibility is expected.
3. When scanner output or advisory data is provided, correlate it with the actual resolved dependency version and reachable usage.
4. Do not claim a CVE from memory alone. Mark advisory status as unverified unless supported by supplied or trusted current documentation.
5. Recommend version pinning, provenance controls, lockfile hygiene, dependency minimization, and review of transitive changes.

## Output

Separate confirmed manifest risks from advisory hypotheses. Include affected package, resolved version when known, evidence location, impact, confidence, and defensive recommendation.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/performing-sca-dependency-scanning-with-snyk`
- `skills/detecting-malicious-npm-packages`
