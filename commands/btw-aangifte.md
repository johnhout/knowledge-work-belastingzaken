---
description: Prepare BTW aangifte workflow and controls
argument-hint: "<tijdvak> [ondernemingsvorm]"
---

# BTW Aangifte / VAT Filing

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Prepare VAT filing workflow for monthly, quarterly, or annual reporting periods.

## Usage

```bash
/belastingadviseur:btw-aangifte <tijdvak> [ondernemingsvorm]
```

## Workflow

1. Confirm reporting scope:
- Period and filing frequency
- Entity type and VAT registration context

2. Gather VAT evidence:
- Sales and purchase data
- Intra-EU/extra-EU relevant transactions
- Corrections and prior period adjustments

3. Build filing draft controls:
- Output VAT vs input VAT mapping
- Exception checks (missing invoices, reverse-charge patterns, unusual balances)
- Reconciliation against bookkeeping totals

4. Official-source verification:
- Verify period deadlines, reporting rules, and procedural requirements on `belastingdienst.nl`
- Verify legal references as needed on `wetten.overheid.nl`
- Record URL and retrieval date per date/rule-sensitive item

5. Fallback behavior:
- If `~~boekhouding` is unavailable, request manual exports and invoice summaries
- If mandatory figures are missing, do not provide filing-ready conclusions
- If official verification fails, label relevant items as unverified

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
