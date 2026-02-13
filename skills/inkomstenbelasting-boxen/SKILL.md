---
name: inkomstenbelasting-boxen
description: This skill should be used when users ask for Dutch income tax support across box 1, box 2, and box 3. Trigger phrases include "IB aangifte", "inkomstenbelasting", "box 1/2/3", "income tax return NL", "voorbereiden aangifte", and "check mijn boxen".
---

# Inkomstenbelasting Boxen

Use this skill to structure IB work with box-level completeness and risk checks.

## Scope

- Box-based classification support (box 1, box 2, box 3)
- Evidence mapping per box
- Filing-readiness checklist and issue flags

## Boundaries

- Do not decide final tax position without verified support.
- Do not provide binding legal interpretation.
- Keep uncertain positions explicitly labeled.

## Workflow

1. Identify income/asset categories and assign box context.
2. Reconcile supplied figures with supporting documents.
3. Flag missing support, anomalies, and prior-year carryover risks.
4. Build stepwise filing-preparation checklist.

## Official Source Verification

For rates, thresholds, criteria, and deadlines:
1. Verify on `belastingdienst.nl`.
2. Verify legal references on `wetten.overheid.nl`.
3. Include URL and retrieval date in outputs.
4. Mark non-verified items as pending professional confirmation.

## Escalation Points

Escalate when:
- Substantial-interest or complex investment structures exist
- Cross-border assets/income exist
- Material discrepancies are unresolved
- Time-sensitive filing risk is high

## Safety

This skill supports tax workflow preparation only and does not provide fiscal advice.
