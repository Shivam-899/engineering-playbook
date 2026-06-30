# Security Policy

## Supported Versions

Only security patches are applied to the following active versions:

| Version | Supported |
| --- | --- |
| 2.x.x | Yes |
| 1.x.x | No |
| < 1.0.0 | No |

---

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security-related bugs.**

If you discover a vulnerability, please report it privately:
1. Email your findings to **security@domain.com**.
2. Include details on how to reproduce the vulnerability, including payload examples, screenshots, or code snippets.
3. We will acknowledge receipt of your vulnerability report within 48 hours and provide a timeline for patch release and disclosure.

---

## Core Security Requirements

For all developers contributing to this project, ensure you adhere to the following standards:

### 🔑 Secret Management
- **Never commit credentials, API keys, or private tokens to the codebase.**
- Use environment variables (`.env`) for local configurations.
- Use a secrets manager (e.g., Vault, AWS Secrets Manager, GCP Secret Manager) in production.

### 💉 Code Injection Prevention
- All user inputs must be validated and sanitized before database insertion or rendering.
- Use parameterized SQL queries / ORM models exclusively to prevent SQL injection.

### 📦 Dependency Scanning
- Ensure dependencies are up-to-date and run audit tools prior to pushing:
  ```bash
  npm audit
  ```
