# Methodology — Risk Scoring & Review Cadence

This document defines how risks in the [risk register](risk-register.md) are scored, rated, and reviewed. The approach follows standard GRC practice and aligns with NIST SP 800-30 risk-assessment concepts.

---

## 1. Scoring model

Each risk is scored on two dimensions, each from **1 to 5**:

**Likelihood** — how probable the risk is to occur:

| Score | Rating | Meaning |
|---|---|---|
| 1 | Rare | Unlikely to occur in normal conditions |
| 2 | Unlikely | Could occur but not expected |
| 3 | Possible | May occur at some point |
| 4 | Likely | Expected to occur |
| 5 | Almost certain | Expected to occur frequently |

**Impact** — the consequence if the risk occurs:

| Score | Rating | Meaning |
|---|---|---|
| 1 | Negligible | Minimal effect on operations |
| 2 | Minor | Limited, short-term effect |
| 3 | Moderate | Noticeable effect; some recovery effort |
| 4 | Major | Significant effect on operations or customers |
| 5 | Severe | Critical effect; major loss or breach |

---

## 2. Risk Score

**Risk Score = Likelihood × Impact** (range 1–25)

| Score | Rating | Color | Review cadence |
|---|---|---|---|
| 15–25 | High | 🔴 Red | Every 30 days |
| 7–14 | Medium | 🟠 Amber | Every 90 days |
| 1–6 | Low | 🟢 Green | Every 180 days |

---

## 3. Residual risk

**Residual Risk** is the risk score re-calculated *after* mitigating controls are applied (Residual Likelihood × Residual Impact).

- Residual risk must be **equal to or lower than** the inherent risk score. If it is higher, the mitigation needs rework.
- A **High residual risk** requires **written risk acceptance from management (ISSM)** before the risk is accepted rather than further treated.

---

## 4. Review cadence

The review date for each risk is driven by its **residual** rating (the real, post-control exposure), using the cadence table in section 2. This ensures effort is focused on the risks that remain most significant after controls.

---

## 5. Risk treatment options

| Option | Description |
|---|---|
| **Mitigate** | Apply controls to reduce likelihood and/or impact |
| **Accept** | Formally accept the residual risk (requires sign-off if High) |
| **Transfer** | Shift risk via insurance or contractual terms |
| **Avoid** | Eliminate the activity that creates the risk |
