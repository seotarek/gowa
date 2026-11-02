# Security Policy

## Threat Model & Scope

GOWA handles sensitive end-to-end encrypted messaging sessions and cryptographic credentials:
- **Session Keys**: WhatsApp session keys stored in SQLite/PostgreSQL databases must be protected with strict filesystem permissions.
- **Webhook Security**: All outbound webhook payloads support HMAC-SHA256 signature verification to prevent spoofing.
- **Network Boundaries**: It is strongly recommended to run GOWA behind an authenticated reverse proxy (Traefik, Nginx) or isolated Docker bridge network.

## Reporting a Vulnerability

To report a vulnerability or credential handling defect:
- Contact `seotarek@gmail.com` with `[SECURITY] GOWA Vulnerability Report`.
- Include reproduction steps and affected endpoints.
- Critical issues receive an acknowledgment within 48 hours.
