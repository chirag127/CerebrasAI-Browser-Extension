# Security Policy for CerebrasAI-BrowserSidekick-ProductivityExtension

As the Apex Technical Authority, this repository adheres to a **Zero-Defect, Proactive Security Posture** aligned with 2026 best practices, especially critical for a browser-side extension handling user data.

## 1. Overview & Philosophy

This project, **CerebrasAI-BrowserSidekick-ProductivityExtension**, is committed to user privacy and security. Since this extension operates heavily client-side (JavaScript/Manifest V3), security focuses intensely on preventing XSS, Supply Chain Attacks, and ensuring secure storage/transmission of sensitive configuration or API keys (if applicable).

**Principles Enforced:**
*   **Principle of Least Privilege (PoLP):** The Manifest V3 permissions are scrutinized and restricted to the absolute minimum required for functionality.
*   **Defense in Depth:** Employing static analysis (Ruff/Biome equivalent for JS/TS, if adopted) and rigorous input sanitization.
*   **Data Minimization:** User data processed by the AI components is handled via secure, ephemeral channels, prioritizing client-side execution where possible.

## 2. Supported Versions

We support the latest stable version of the codebase and actively backport critical security fixes to the previous major release branch (`release/v1.x`) for 90 days post-release.

*   **Active Support:** `main` branch (Development) and latest tagged release.
*   **Maintenance Mode:** Patches only for `v1.x` releases.

## 3. Reporting a Vulnerability

We value the security community's contribution to maintaining the integrity of this high-performance tool. Please follow these steps for responsible disclosure:

### A. Scope & Sensitivity

1.  **Do NOT** publicly disclose any vulnerability (e.g., open a public Issue or discuss on social media) before the coordinated disclosure timeline is complete.
2.  **Sensitive Data:** If you have discovered a vulnerability that involves accessing user data, encryption keys, or proprietary algorithms, **DO NOT** include proof-of-concept exploits in your initial report.

### B. Disclosure Steps

1.  **Initial Contact:** Email the security contact immediately:
    *   **Security Contact Email:** `security+cerebraisidekick@chirag127.dev` (This is a placeholder; actual contact information should be managed via GitHub Security Advisories).
2.  **Report Content:** Your report should include:
    *   A clear, descriptive title.
    *   The affected component/file path.
    *   Steps to reproduce (if applicable, use non-exploitative methods).
    *   Severity assessment (CVSS score if known).

## 4. Vulnerability Disclosure Timeline (Coordinated Effort)

We adhere to a structured, time-bound process to ensure swift remediation while protecting users:

| Phase | Duration (from Report Receipt) | Action Required |
| :--- | :--- | :--- |
| **Triage & Confirmation** | 48 Hours | Security team validates the report. |
| **Fix Development** | 14 Days (Standard) | Developer team implements the fix. |
| **Pre-Release Testing** | 3 Days | Fix is tested in staging/pre-release environment. |
| **Coordinated Disclosure** | Day 17-21 | Patch is released via a new extension version on all relevant stores. Public acknowledgement is made. |

*Note: Extensions to the timeline may occur for highly complex vulnerabilities, in which case you will be notified.* 

## 5. Security Best Practices for Users

Users are encouraged to follow these practices when using the extension:

1.  **Source Verification:** Only install the extension from the official Chrome Web Store or Firefox Add-ons store, or directly from the source repository's release assets if self-hosting.
2.  **Permissions Review:** Regularly review the extension permissions in your browser settings.
3.  **Updates:** Keep your browser and extension updated to receive the latest security patches.

## 6. Scanning and Tooling

To maintain the Apex standard, automated security scanning is integrated into our CI/CD pipeline (`.github/workflows/ci.yml`):

*   **Static Analysis:** Integration with relevant JavaScript/TypeScript security scanners (e.g., Snyk integration or equivalent dependency checking) to catch vulnerabilities in third-party libraries.
*   **Dependency Auditing:** Dependencies are audited on every pull request to ensure zero known critical vulnerabilities are introduced. (Refer to the `AGENTS.md` for specific tooling requirements for this stack).

***
*Last Updated: December 2025*

[Back to Repository Root](https://github.com/chirag127/CerebrasAI-BrowserSidekick-ProductivityExtension)