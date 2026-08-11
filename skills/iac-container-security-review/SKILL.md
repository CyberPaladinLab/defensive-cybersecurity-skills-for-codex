---
name: iac-container-security-review
description: "Read-only review of Docker, Kubernetes, Terraform, Compose, and related IaC for defensive configuration risks."
---

# IaC and Container Security Review

## Safety boundary

Do not build images, pull images, apply infrastructure, connect to clusters, alter cloud resources, or run scanners.

## Review workflow

1. Inspect Dockerfiles, Compose, Kubernetes manifests, Terraform, Helm values, and related configuration in scope.
2. Check for privileged containers, host namespace or socket exposure, risky mounts, excessive Linux capabilities, root execution, writable root filesystems, missing resource limits, insecure secret placement, broad network exposure, and weak image provenance.
3. Review cloud/IaC permissions for wildcards, public access, unencrypted sensitive storage, unsafe defaults, and overly broad trust policies.
4. Treat environment-specific assumptions explicitly; do not infer deployed state from templates alone.
5. Recommend least privilege, immutable artifacts, explicit network boundaries, secret separation, and safer runtime defaults.

## Output

Report resource/file location, risky setting, threat consequence, confidence, and a defensive configuration recommendation. Do not apply it.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/scanning-iac-and-images-with-trivy`
- `skills/implementing-infrastructure-as-code-security-scanning`
- `skills/scanning-docker-images-with-trivy`
