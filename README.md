# Defensive Cybersecurity Safe

A small defensive-only Codex plugin assembled with an allowlist from the audited `Anthropic-Cybersecurity-Skills` snapshot.

## Contents

Twenty concise, read-only skills cover secure code review, vulnerability triage, SAST design, secret exposure, dependency and SBOM review, CI/CD and supply-chain provenance, API/OAuth/WebSocket security, cryptography, security headers, privacy, logging, serverless, containers, IaC, and threat modeling.

The package contains no `scripts/`, hooks, MCP servers, apps, installers, active scanners, exploit workflows, credential-access helpers, external upload functions, or write automation. Operational upstream content was not copied; retained defensive concepts were rewritten under `POLICY.md`.

## Safety model

- Read-only analysis of user-authorized local artifacts.
- No command execution, installation, network probing, external upload, or infrastructure mutation.
- No credential retrieval or validation.
- Evidence-backed reporting with sensitive values redacted.

Inspect `POLICY.md`, `MANIFEST.json`, and the individual `skills/*/SKILL.md` files before installation. Install this curated package only; do not substitute or auto-update from the upstream `main` branch.
