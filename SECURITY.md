# Security Policy

Do not report credential, authentication, authorization, payment or private-data vulnerabilities in a public issue.

Report security concerns privately to **hello@twe.co.ke**.

Production secrets must be loaded from `.env` and must never be committed.

The following must never be committed:

- database passwords
- payment secret keys
- email-provider API keys
- private Firebase service credentials
- session or encryption secrets
- private certificates
- access tokens
- production database exports containing user data

If a secret is committed, rotate it immediately. Deleting it in a later commit does not make the exposed credential safe.
