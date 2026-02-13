---
description: Build Dutch tax intake and dossier baseline
argument-hint: "<profieltype> [belastingjaar]"
---

# Intake / Intake

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Create a complete intake for Dutch tax work and prepare a dossier that can support follow-up filings.

## Usage

```bash
/belastingadviseur:intake <profieltype> [belastingjaar]
```

## Workflow

1. Identify profile and context:
- Profieltype/Profile: `particulier`, `zzp`, or `bv`
- Tax year and reporting periods
- Residency, household, and business structure context

2. Build obligations map:
- Identify likely obligations (IB, BTW, VPB, loonheffingen, other)
- Mark which obligations are in scope and out of scope

3. Collect required evidence:
- Request source documents, statements, prior filings, and notices
- Track missing items and blocking dependencies

4. Connector-aware retrieval:
- If `~~boekhouding`, `~~salarisadministratie`, `~~documentopslag`, `~~email`, or `~~data warehouse` is connected, pull available records
- If not connected, ask user to provide data manually using the same checklist

5. Set risk and escalation flags:
- Missing mandatory documents
- Complex ownership/international factors
- Conflicting figures across sources
- Prior-year unresolved items

6. Source verification rule:
- Before mentioning statutory deadlines, rates, or legal criteria, verify on `belastingdienst.nl` and/or `wetten.overheid.nl`
- Add URL and retrieval date (`YYYY-MM-DD`)

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
