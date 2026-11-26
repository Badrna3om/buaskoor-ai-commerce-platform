# Security Notes

Before production:
- Keep credentials in n8n credentials or environment variables.
- Remove all pinned customer data.
- Validate webhooks.
- Add rate limits.
- Use minimum WooCommerce permissions.
- Restrict Telegram access.
- Minimize customer data.
- Add retention, monitoring, backups, and failure alerts.

## Public Portfolio Review — 26 November 2026

This repository's checked-out tracked files were inspected with a **bounded static scan** for common hard-coded GitHub, OpenAI, AWS, Telegram, JWT, private-key and Authorization token formats. No direct match was found in the inspected files. This is **not** a complete security assessment, a full Git-history audit, or proof that no sensitive operational details were ever published.

**Deployment boundary:** Customer contact and checkout integrations must enforce webhook authentication, session privacy and WooCommerce least-privilege permissions.

Do not push real credentials, customer transactions or deployment secrets into this public repo. A `.gitignore` helps prevent accidental future additions but **does not hide files already committed**. Rotate any credential discovered in a public commit or log.

The public examples are designed for code review and demonstration. Operational deployments require separate environment review and verification.
