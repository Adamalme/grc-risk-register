# Control Mapping — SOC 2 / ISO 27001 / NIST 800-53

This maps the mitigating controls from the [risk register](risk-register.md) to three common frameworks, showing how a single control satisfies requirements across all of them. This is the "write once, demonstrate many" value of cross-framework mapping.

- **SOC 2** — Trust Services Criteria (TSC)
- **ISO/IEC 27001:2022** — Annex A controls
- **NIST SP 800-53 Rev. 5** — control families

All mappings use public framework references. Mappings are illustrative and would be validated against the current control catalog in a real engagement.

---

## Control-to-framework matrix

| Control | What it does | Risks addressed | SOC 2 (TSC) | ISO 27001:2022 | NIST 800-53 |
|---|---|---|---|---|---|
| Multi-Factor Authentication (MFA) | Requires a second factor for authentication | R-001, R-003, R-010 | CC6.1 | A.5.17, A.8.5 | IA-2, IA-2(1) |
| Least-privilege IAM & access reviews | Grants minimum access; reviews it periodically | R-001, R-011 | CC6.1, CC6.3 | A.5.15, A.5.18 | AC-2, AC-6 |
| Vulnerability management & remediation SLAs | Scans and fixes known vulnerabilities on a timeline | R-002 | CC7.1 | A.8.8 | RA-5, SI-2 |
| Security awareness training | Trains staff to recognize phishing and threats | R-003 | CC2.2 | A.6.3 | AT-2 |
| Backups with restore testing (3-2-1) | Keeps recoverable copies; verifies they restore | R-004 | A1.2 | A.8.13 | CP-9, CP-10 |
| Vendor security review (TPRM) | Assesses third-party security before/while sharing data | R-005 | CC9.2 | A.5.19, A.5.20 | SA-9, PM-9 |
| Configuration monitoring & IaC guardrails | Detects and prevents insecure configurations | R-006 | CC7.1 | A.8.9 | CM-2, CM-6 |
| Secret scanning in CI | Detects secrets before they reach a repo | R-008 | CC8.1 | A.8.28 | SA-11, SA-15 |
| Compliance calendar & evidence management | Ensures recurring controls run and are evidenced | R-009 | CC4.1 | A.5.35, A.5.36 | CA-7, AU-6 |
| Logging & monitoring | Records and reviews security-relevant events | R-002, R-011 | CC7.2 | A.8.15, A.8.16 | AU-2, AU-6, SI-4 |
| Dual approval for financial payouts | Requires two people to authorize payments | R-010 | CC6.1 | A.5.3 | AC-5 |
| Domain registrar lock & auto-renew | Protects domain ownership and continuity | R-012 | A1.2 | A.5.9 | CM-8, CP-2 |

---

## How to read this

Each row is **one control** an organization implements once. The three right-hand columns show which requirement that control satisfies in each framework. For example, implementing **MFA** gives you evidence for **SOC 2 CC6.1**, **ISO 27001 A.8.5**, *and* **NIST IA-2** at the same time — so a company pursuing all three doesn't do the work three times.

This cross-mapping is the backbone of an efficient multi-framework compliance program and is exactly what GRC platforms (and the Secure Controls Framework) automate at scale.
