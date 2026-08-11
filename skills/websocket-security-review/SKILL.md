---
name: websocket-security-review
description: "Read-only review of WebSocket server code and configuration for handshake, origin, authentication, authorization, message-validation, privacy, and resource-exhaustion risks."
---

# WebSocket Security Review

Follow the package-wide `POLICY.md`. Review only supplied code, configuration, logs, and architecture. Do not connect to an endpoint, send frames, fuzz messages, create attack pages, or perform load testing.

1. Trace the HTTP upgrade and authentication flow, including token/cookie handling, origin validation, subprotocol negotiation, TLS assumptions, and reconnect behavior.
2. Verify authorization for every message type and object identifier; connection-level authentication alone is insufficient.
3. Review schema validation, size limits, decompression, binary/text handling, serialization, and output encoding.
4. Check per-connection and per-identity limits, backpressure, queue bounds, idle timeouts, fan-out, replay resistance, and cleanup after disconnect.
5. Inspect logs and error frames for tokens, cookies, internal identifiers, stack traces, or cross-tenant data.

Report evidence location, trust boundary, impact, confidence, and defensive remediation. Do not provide operational bypass or denial-of-service instructions.

Curated from the defensive design concerns in upstream `skills/testing-websocket-api-security`; no upstream scripts, payloads, active-test instructions, or external-upload examples are included.
