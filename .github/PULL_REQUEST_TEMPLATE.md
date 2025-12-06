# 🚀 Pull Request Template: Apex Standard Review

## 🎯 Overview

<!-- Briefly summarize the changes. Why is this PR necessary? Reference issue numbers if applicable (e.g., Fixes #123, Implements #456). -->

## 🧠 Architectural Context

This PR aligns with the **Zero-Defect, High-Velocity, Future-Proof** philosophy. All changes must adhere to Manifest V3 compliance, strict separation of concerns (e.g., separating background scripts from content scripts), and absolute security for client-side operations.

### Checklist

* [ ] **Breaking Change?** (If yes, detail impact below)
* [ ] **New Feature?** (Describe functionality)
* [ ] **Bug Fix?** (Describe defect addressed)
* [ ] **Documentation Update?**
* [ ] **Code Style/Linting Fix?** (Should be auto-fixed by Biome/Ruff equivalent)
* [ ] **Tests Added/Updated?** (Crucial for extension logic)

---

## 📝 Detailed Description

<!-- Provide a comprehensive description of the changes. If this involved architectural shifts (e.g., moving state management, updating API calls), document them clearly here. -->

### Manifest V3 Compliance Check

- [ ] Have background tasks been moved to Service Workers?
- [ ] Are all permissions scoped and justified?

## 🧪 Verification Steps (QA)

Describe the exact steps required to test this change thoroughly. For browser extensions, this must include environment details.

1.  **Environment:** Browser (Chrome/Firefox/Edge), Version:
2.  **Setup:** Load unpacked extension from branch `{{BRANCH_NAME}}`.
3.  **Action 1:** [Describe user action]
4.  **Expected Result 1:** [Describe expected outcome]
5.  **Action 2:** [Describe edge case/error path]
6.  **Expected Result 2:** [Describe expected robust handling]

---

## 🚧 Related Issues

Closes: (If this PR closes any associated GitHub Issues)

## 📸 Screenshots / Demos (If applicable)

<!-- Use screenshots or GIFs for UI/UX related changes. -->

--- 

## 🤖 Agent Directives Alignment

This submission adheres to the standards defined in `.github/AGENTS.md`. The core logic follows **SOLID principles** (specifically SRP for isolation of AI vs. DOM interaction) and maintains high **DRY** standards in utility functions.

**Architectural Note:** If the change touches the AI summarization engine, ensure the prompt engineering template (if applicable) is resilient against context drift.
