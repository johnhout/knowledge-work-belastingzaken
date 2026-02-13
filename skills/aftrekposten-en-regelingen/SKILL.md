---
name: aftrekposten-en-regelingen
description: This skill should be used when users ask for deduction checks, allowance eligibility, or tax-regime qualification for Dutch filings. Trigger phrases include "aftrekposten", "deduction check", "kom ik in aanmerking", "tax credit NL", and "regeling controle".
---

# Aftrekposten en Regelingen

Use this skill to assess deduction opportunities and qualification requirements with evidence discipline.

## Scope

- Deduction candidate identification
- Eligibility and evidence checklist generation
- Confidence ranking and blocker detection

## Boundaries

- Do not confirm eligibility as final without full verification.
- Do not provide binding legal interpretation.
- Keep uncertain or partial cases explicitly labeled.

## Workflow

1. Capture user profile and factual context.
2. Map potential deductions/regimes to evidence requirements.
3. Validate completeness and identify weak support.
4. Produce prioritized next actions.

## Official Source Verification

1. Verify criteria, limits, and timelines on `belastingdienst.nl`.
2. Verify legal references on `wetten.overheid.nl` when relevant.
3. Include URL + retrieval date for all rule-dependent statements.
4. Mark non-verified items as pending.

## Escalation Points

Escalate when:
- Qualification depends on nuanced legal interpretation
- Multiple regimes conflict
- Missing evidence could materially change outcome

## Safety

This skill supports preparation and does not replace qualified tax advice.
