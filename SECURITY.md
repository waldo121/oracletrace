# Security Policy

## Supported Versions

OracleTrace follows a simple support model focused on stability and active development.

Only the most recent minor version within the latest major release line receives security updates.

| Version   | Supported          |
|-----------|--------------------|
| 2.x (latest) | :white_check_mark: |
| < 2.0     | :x:                |

> Note: Pre-release and development versions are not guaranteed to receive security fixes.

---

## Security Scope

OracleTrace is a **local execution profiling tool**. It does not:

* Execute remote code
* Open network sockets
* Persist sensitive data outside user-defined outputs (JSON/CSV)

Security considerations are primarily related to:

* Execution of untrusted Python scripts
* File system access during profiling
* Handling of generated trace artifacts

Users are responsible for ensuring that the profiled scripts are trusted.

---

## Reporting a Vulnerability

If you discover a security vulnerability, report it responsibly.

### Preferred Method

Open a **private security advisory** via GitHub:

👉 https://github.com/KaykCaputo/oracletrace/security/advisories

### Alternative

If private advisory is not available, open an issue labeled: `[SECURITY]`

Avoid including exploit details publicly until the issue is assessed.

---

## What to Include

Provide as much technical detail as possible:

* Description of the vulnerability
* Steps to reproduce
* Proof of concept (PoC), if applicable
* Impact assessment (e.g., code execution, data exposure)
* Affected versions

---

## Response Timeline

Typical handling process:

* **Initial acknowledgment:** within 48 hours
* **Assessment and triage:** 2–5 days
* **Fix (if confirmed):** depends on severity and complexity
* **Disclosure:** coordinated after patch release

---

## Resolution Policy

If the vulnerability is accepted:

* A fix will be developed and released in the latest supported version
* Release notes will include a security section
* Credit will be given when appropriate

If declined:

* A clear technical justification will be provided

---

## Security Best Practices

When using OracleTrace:

* Do not profile untrusted or unknown scripts
* Avoid running with elevated privileges
* Review generated JSON/CSV outputs before sharing
* Use isolated environments (e.g., virtualenv)

---

## Dependency Management

OracleTrace relies on a minimal dependency set:

* `rich` for CLI output rendering

Dependencies are monitored and updated when security issues are identified.

---

## Disclosure Policy

OracleTrace follows **responsible disclosure**:

* No public disclosure before a fix is available
* Coordinated release of patch and advisory
* Transparent changelog entries for security fixes

---

## Contact

Maintainers:

* Kayk Caputo  
* André Gustavo  

For direct contact, prefer GitHub channels associated with the repository.
