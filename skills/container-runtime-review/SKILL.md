---
name: container-runtime-review
description: "Read-only review of Dockerfile, Compose, OCI, and container runtime configuration for privilege, isolation, filesystem, capability, resource, provenance, and secret-handling risks."
---

# Container Runtime Review

Follow `POLICY.md`. Do not build, pull, run, inspect, or modify containers, images, hosts, registries, or daemon settings.

1. Review base-image pinning, build context, copied artifacts, package installation, build secrets, users, entrypoints, and multi-stage boundaries.
2. Check runtime user, capabilities, privileged mode, host namespaces, Docker socket/device mounts, seccomp/AppArmor assumptions, filesystem mutability, and temporary storage.
3. Review port exposure, network attachment, resource and process limits, health checks, restart behavior, and logging.
4. Identify secrets in layers, environment variables, labels, commands, or Compose files.
5. Distinguish image configuration from deployed runtime state and state all unknowns.

Report configuration evidence, violated isolation boundary, impact, confidence, and defensive recommendation.

Curated from upstream `skills/hardening-docker-containers-for-production`; daemon changes, Docker commands, host auditing, installers, and scripts are excluded.
