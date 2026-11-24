# Risk Register — Nimbus SaaS Co.

Information security risk register for a fictional early-stage SaaS company pursuing SOC 2 Type II and preparing for ISO/IEC 27001. Scoring follows the [methodology](methodology.md): Risk Score = Likelihood × Impact (1–25).

- **Rating thresholds:** 15–25 High 🔴 · 7–14 Medium 🟠 · 1–6 Low 🟢
- **Review cadence** is driven by the **residual** rating.
- All data is synthetic. No real identifiers, accounts, or confidential content.

---

## Register

| Risk ID | Category | Description (threat → asset → impact) | L | I | Score | Rating | Mitigation | Owner | Res. L | Res. I | Residual | Review |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | Security | Compromised cloud admin credentials allow an attacker to access customer data | 4 | 5 | 20 | 🔴 High | Enforce MFA on all admin accounts; least-privilege IAM; access reviews | ISSM | 2 | 5 | 10 🟠 | 90 days |
| R-002 | Security | Unpatched known vulnerability on a public-facing host is exploited | 4 | 4 | 16 | 🔴 High | Monthly vulnerability scanning; 15-day remediation SLA for criticals | ISSE | 2 | 4 | 8 🟠 | 90 days |
| R-003 | Security | Phishing attack leads to employee account takeover | 4 | 3 | 12 | 🟠 Medium | Security awareness training; email filtering; MFA | ISSO | 2 | 3 | 6 🟢 | 180 days |
| R-004 | Business | Incomplete or failed backup causes loss of customer files with no recovery | 3 | 4 | 12 | 🟠 Medium | Automated backups with versioning; quarterly restore tests (3-2-1 rule) | IT Lead | 2 | 2 | 4 🟢 | 180 days |
| R-005 | Vendor | Critical SaaS vendor suffers a breach, exposing shared data | 3 | 4 | 12 | 🟠 Medium | Vendor security reviews (SOC 2 collection); contractual security terms | ISSO | 2 | 3 | 6 🟢 | 180 days |
| R-006 | Security | Misconfigured storage bucket exposes data publicly | 3 | 5 | 15 | 🔴 High | IaC guardrails; config monitoring; block public access by default | ISSE | 1 | 5 | 5 🟢 | 180 days |
| R-007 | Business | Single-person dependency on a key engineer creates a knowledge/availability gap | 4 | 3 | 12 | 🟠 Medium | Documentation; cross-training; access continuity plan | People Ops | 2 | 3 | 6 🟢 | 180 days |
| R-008 | Security | Secrets (API keys) committed to a public code repository | 3 | 4 | 12 | 🟠 Medium | Secret scanning in CI; pre-commit hooks; key rotation | ISSE | 1 | 4 | 4 🟢 | 180 days |
| R-009 | Compliance | Missing or stale evidence causes SOC 2 audit findings | 3 | 3 | 9 | 🟠 Medium | Compliance calendar; evidence automation; quarterly reviews | ISSO | 2 | 2 | 4 🟢 | 180 days |
| R-010 | Business | Payment provider account takeover enables fraudulent transactions | 2 | 5 | 10 | 🟠 Medium | MFA on financial accounts; dual approval for payouts | Finance | 1 | 5 | 5 🟢 | 180 days |
| R-011 | Security | Insider inappropriately accesses customer data beyond their role | 2 | 4 | 8 | 🟠 Medium | Least-privilege access; logging and monitoring; quarterly access reviews | ISSO | 1 | 4 | 4 🟢 | 180 days |
| R-012 | Vendor | Domain registrar lapse causes loss of domain and service outage | 2 | 4 | 8 | 🟠 Medium | Auto-renew; registrar lock; monitored expiry alerts | IT Lead | 1 | 4 | 4 🟢 | 180 days |

---

## Top 5 risks (by inherent score)

| Rank | Risk ID | Description | Inherent | Residual |
|---|---|---|---|---|
| 1 | R-001 | Compromised cloud admin credentials | 20 🔴 | 10 🟠 |
| 2 | R-002 | Unpatched public-facing vulnerability | 16 🔴 | 8 🟠 |
| 3 | R-006 | Misconfigured public storage bucket | 15 🔴 | 5 🟢 |
| 4 | R-003 | Phishing → account takeover | 12 🟠 | 6 🟢 |
| 5 | R-004 | Backup failure → data loss | 12 🟠 | 4 🟢 |

---

## Notes

- No risk currently carries a **High residual** rating, so no written management (ISSM) acceptance is required at this time.
- R-001 remains the highest residual exposure (Medium) and is reviewed on a 90-day cadence.
- Owners are named by **role**, not individual, per data-handling practice for a public document.
