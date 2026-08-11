# Defensive Cybersecurity Skills for Codex

A curated, defensive-only cybersecurity skill pack for OpenAI Codex.

Built from defensive concepts found in the audited
`mukul975/Anthropic-Cybersecurity-Skills` snapshot and rewritten under strict read-only safety boundaries.

## What is this?

The original upstream collection contains hundreds of cybersecurity skills, including defensive, dual-use, and offensive workflows.

This repository contains a deliberately small allowlisted subset designed for users who want Codex to review software security without giving it offensive or system-modifying workflows.

## Included

20 defensive security skills covering:

- Secure code review
- Secret exposure review
- Dependency risk review
- SBOM review
- SAST rule review
- CI/CD security review
- Supply-chain provenance review
- Container runtime review
- Infrastructure-as-Code review
- API authentication review
- OAuth/OIDC scope review
- WebSocket security review
- Cryptography review
- Security headers review
- Privacy and sensitive-data flow review
- Logging and telemetry review
- Serverless security review
- Threat modeling
- Web vulnerability triage
- Container/IaC security review

## Safety model

This pack is intentionally restricted to defensive, read-only analysis.

It contains:

- No executable scripts
- No MCP servers
- No apps
- No installers
- No active scanners
- No arbitrary shell or PowerShell execution
- No credential retrieval or validation
- No phishing workflows
- No command-and-control workflows
- No persistence techniques
- No privilege escalation
- No lateral movement
- No exploit or payload generation
- No destructive actions
- No external source-code uploads
- No system, cloud, firewall, IAM, or infrastructure modification

If a requested task requires active probing, credential access, command execution, external upload, or system modification, the skills are instructed to stop rather than perform the action.

See [`POLICY.md`](POLICY.md) for the complete safety policy.

## Repository structure

```text
.
├── .codex-plugin/
│   └── plugin.json
├── skills/
│   └── <20 defensive skills>/
│       └── SKILL.md
├── LICENSE
├── MANIFEST.json
├── NOTICE
├── POLICY.md
├── README.md
├── SHA256SUMS.txt
└── SOURCE_SNAPSHOT.md
```

## Installation

### Codex desktop

Download the release ZIP and inspect it before installation.

For direct personal-skill installation on macOS:

```bash
mkdir -p ~/.agents/skills
cp -R skills/* ~/.agents/skills/
```

Restart Codex after installation.

Personal Skills may need to be installed separately across supported ChatGPT/Codex surfaces; they do not necessarily sync automatically between desktop and web/mobile.

### Plugin package

The repository also contains:

```text
.codex-plugin/plugin.json
```

for environments that support the Codex plugin package format.

## Verified release

Current release:

**v0.1.0**

Release archive:

```text
defensive-cybersecurity-safe-codex-plugin.zip
```

SHA-256:

```text
095fd8c2d97663cf64c023873df05e08a948b27abeedd938b58e5cb7806f24fd
```

Verify on macOS:

```bash
shasum -a 256 defensive-cybersecurity-safe-codex-plugin.zip
```

The output should match the hash above exactly.

## Provenance

Source repository:

`mukul975/Anthropic-Cybersecurity-Skills`

Audited source commit:

```text
4c0b700ac5d280ba46695062077f0fe922ce3602
```

The package does not copy operational upstream workflows verbatim.

Defensive concepts were selected and rewritten under the policy in [`POLICY.md`](POLICY.md).

See:

- [`MANIFEST.json`](MANIFEST.json) — selected skills and source mappings
- [`SOURCE_SNAPSHOT.md`](SOURCE_SNAPSHOT.md) — audited source snapshot
- [`NOTICE`](NOTICE) — attribution
- [`SHA256SUMS.txt`](SHA256SUMS.txt) — integrity information

## Important security note

No security package should be trusted only because it describes itself as safe.

Before installing:

1. Inspect the repository.
2. Review `POLICY.md`.
3. Review the individual `SKILL.md` files.
4. Verify the release SHA-256.
5. Install only the fixed release you reviewed.

The safety assessment applies to the reviewed release and its exact contents. Future changes should be reviewed independently.

## License

Apache License 2.0.

See [`LICENSE`](LICENSE).

## Disclaimer

This is an unofficial community project.

It is not affiliated with or endorsed by OpenAI, Anthropic, or the maintainers of the upstream repository.

Use only on systems, code, and data you are authorized to review.
