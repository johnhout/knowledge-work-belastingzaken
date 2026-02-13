---
name: belasting-intake-en-dossiervorming
description: This skill should be used when users ask for a Dutch tax intake, dossier setup, document checklist, or obligation mapping for particulier, ZZP, or BV contexts. Trigger phrases include "belasting intake", "tax intake", "welke documenten heb ik nodig", "build my tax dossier", and "map mijn aangifteplichten".
---

# Belasting Intake en Dossiervorming

Use this skill to create a structured intake baseline and an evidence-complete tax dossier.

## Scope

- Intake for `particulier`, `zzp`, and `bv`
- Obligation mapping (IB, BTW, VPB, loonheffingen)
- Document completeness and blocker tracking

## Boundaries

- Do not provide final legal or fiscal advice.
- Do not assume obligations without stating assumptions.
- Do not present unverified legal/rate/deadline claims as final.

## Workflow

1. Capture taxpayer profile, year, and filing context.
2. Build obligation map and identify in-scope taxes.
3. Produce a document checklist with missing-item tracking.
4. Mark dependencies and unresolved data gaps.

## Official Source Verification

Before any rule-dependent claim:
1. Verify procedural and practical requirements on `belastingdienst.nl`.
2. Verify legal basis wording on `wetten.overheid.nl` where applicable.
3. Record URL + retrieval date (`YYYY-MM-DD`).
4. Label as "unverified" if no official confirmation is available.

## Escalation Points

Escalate to a qualified advisor when:
- Cross-border, migration, or treaty context appears
- Ownership/entity structure is complex
- Source data conflicts materially
- Filing consequences are high impact

## Safety

This skill supports workflows only and does not replace professional tax advice.
