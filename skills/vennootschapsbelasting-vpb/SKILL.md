---
name: vennootschapsbelasting-vpb
description: This skill should be used when users need Dutch corporate income tax workflow support for BV entities. Trigger phrases include "VPB aangifte", "vennootschapsbelasting", "corporate tax NL", "fiscal profit bridge", and "voorbereiden VPB".
---

# Vennootschapsbelasting VPB

Use this skill for VPB dossier preparation and pre-filing controls.

## Scope

- BV VPB workflow planning
- Fiscal bridge from accounting result to taxable profit
- Evidence mapping for adjustments and schedules

## Boundaries

- Do not provide final legal/fiscal determinations.
- Do not assume treatment of complex transactions without explicit caveats.
- Keep uncertain tax positions flagged for advisor review.

## Workflow

1. Establish entity and book-year context.
2. Gather financial source data and prior-year context.
3. Build adjustment mapping with traceable evidence.
4. Flag uncertain positions, missing support, and deadlines.

## Official Source Verification

1. Verify filing process and deadlines on `belastingdienst.nl`.
2. Verify statutory references on `wetten.overheid.nl`.
3. Cite URL and retrieval date in output.
4. If unverifiable, classify as pending verification.

## Escalation Points

Escalate when:
- Fiscal unity, mergers, restructurings, or cross-border elements exist
- Material uncertain positions affect filing outcome
- Evidence is incomplete near filing deadlines

## Safety

This skill supports VPB workflows only and does not replace professional tax advice.
