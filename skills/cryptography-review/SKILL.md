---
name: cryptography-review
description: "Read-only cryptographic design and implementation review for unsafe primitives, key handling, randomness, storage, and protocol misuse."
---

# Cryptography Review

## Safety boundary

Do not access keychains, HSMs, credential stores, private keys, encrypted user data, or remote key-management systems. Do not attempt decryption of protected data.

## Review workflow

1. Identify cryptographic primitives, modes, key derivation, password hashing, signature verification, randomness, nonce/IV generation, certificate validation, and key lifecycle code.
2. Look for deprecated or unauthenticated encryption, constant keys, predictable randomness, nonce reuse, missing integrity checks, insecure password hashing parameters, verification bypasses, and accidental key material in source or logs.
3. Check protocol sequencing and whether authentication/authorization decisions depend on unverified data.
4. Distinguish implementation bugs from policy choices and document assumptions about external key management.
5. Recommend established high-level constructions rather than custom cryptography.

## Output

Report affected code/config, primitive or design issue, security consequence, confidence, and a defensive remediation recommendation. Redact any sensitive material.

## Curated source references

This is a sanitized derivative conceptually informed by the following paths in the pinned source snapshot; no source scripts are included and the original operational instructions were not copied verbatim:
- `skills/performing-cryptographic-audit-of-application`
