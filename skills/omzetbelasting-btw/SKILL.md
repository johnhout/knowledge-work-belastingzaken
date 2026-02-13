---
name: omzetbelasting-btw
description: This skill should be used when users ask about BTW workflows, periodic VAT filing preparation, input/output VAT checks, ICP questions, or correction handling. Trigger phrases include "btw aangifte", "omzetbelasting", "VAT return NL", "voorbelasting", "ICP", and "btw correctie".
---

# Omzetbelasting BTW

Use this skill to run VAT preparation with period controls and evidence traceability.

## Scope

- Monthly/quarterly/annual BTW preparation
- Input/output VAT control checks
- Data quality checks and correction tracking

## Boundaries

- Do not finalize filing decisions without evidence completeness.
- Do not provide definitive legal advice.
- Keep all unresolved VAT treatment questions explicitly open.

## Workflow

1. Confirm period, registration context, and transaction profile.
2. Reconcile sales/purchase evidence to VAT categories.
3. Identify anomalies and missing invoice support.
4. Produce filing readiness output with risk notes.

## Official Source Verification

1. Verify filing deadlines and practical instructions on `belastingdienst.nl`.
2. Verify legal wording when needed on `wetten.overheid.nl`.
3. Log URL + retrieval date for each rule-sensitive statement.
4. Mark unverifiable claims as non-final.

## Escalation Points

Escalate when:
- Cross-border VAT treatment is uncertain
- Reverse-charge or special regime treatment is unclear
- Material period-over-period deviations lack explanation
- High-value corrections are needed

## Safety

This skill supports process quality and does not replace professional fiscal advice.
