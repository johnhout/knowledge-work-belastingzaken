---
description: Prepare loonheffingen workflow and WKR checks
argument-hint: "<tijdvak>"
---

# Loonheffingen / Payroll Taxes

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Prepare payroll tax workflow including periodic controls and WKR attention points.

## Usage

```bash
/belastingadviseur:loonheffingen <tijdvak>
```

## Workflow

1. Confirm payroll scope:
- Reporting period and employer entity
- Active payroll setups and known exceptions

2. Gather payroll evidence:
- Payroll runs, wage summaries, and benefits overview
- WKR-related expense data and categorization support

3. Control framework:
- Reconcile payroll tax totals with payroll administration
- Check unusual deviations by period and employee groups
- Flag potential WKR or classification issues for review

4. Official-source verification:
- Verify payroll filing timing and procedural obligations on `belastingdienst.nl`
- Verify legal interpretation references on `wetten.overheid.nl` where needed
- Capture URL and retrieval date

5. Fallback behavior:
- If `~~salarisadministratie` is not connected, request period export files
- If evidence is incomplete, classify as non-final draft
- If official verification cannot be completed, mark affected guidance as unverified

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
