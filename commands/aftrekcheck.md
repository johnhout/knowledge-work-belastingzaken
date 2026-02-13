---
description: Validate deductions and eligibility evidence
argument-hint: "<belastingjaar> [doelgroep]"
---

# Aftrekcheck / Deduction Check

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Assess potential deductions and scheme eligibility for individual and business contexts.

## Usage

```bash
/belastingadviseur:aftrekcheck <belastingjaar> [doelgroep]
```

## Workflow

1. Define taxpayer context:
- Individual household context, ZZP context, or BV context
- Financial and operational facts relevant to deductions

2. Build deduction candidate list:
- Identify likely relevant deduction categories
- Distinguish high-confidence vs uncertain candidates

3. Evidence and eligibility validation:
- Map every candidate to required supporting documents
- Flag missing evidence or conflicting data

4. Official-source verification:
- Verify qualification criteria, thresholds, and limitations on `belastingdienst.nl`
- Verify legal references on `wetten.overheid.nl` when statutory wording matters
- Cite exact URL and retrieval date

5. Fallback behavior:
- Without connectors, use user-provided data with clear assumptions
- Do not label any deduction as final if key eligibility or source verification is missing

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
