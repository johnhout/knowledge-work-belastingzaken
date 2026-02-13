---
description: Prepare VPB workflow with fiscal control checks
argument-hint: "<boekjaar>"
---

# VPB Aangifte / Corporate Income Tax Filing

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Prepare vennootschapsbelasting workflow for BV entities with evidence mapping and risk checks.

## Usage

```bash
/belastingadviseur:vpb-aangifte <boekjaar>
```

## Workflow

1. Confirm entity and year context:
- Book year and entity details
- Special circumstances (fiscal unity, restructuring, cross-border activity)

2. Gather source records:
- Trial balance and annual accounts
- Prior assessments and carryforwards
- Supporting schedules for material tax adjustments

3. Build fiscal bridge:
- Commercial result to fiscal profit mapping
- Adjustment categories and evidence traceability
- Flag uncertain positions for escalation

4. Official-source verification:
- Verify filing deadlines and process instructions on `belastingdienst.nl`
- Verify legal references and article citations on `wetten.overheid.nl`
- Add URL and retrieval date for each legal or rule-sensitive assertion

5. Fallback behavior:
- If `~~data warehouse` or `~~boekhouding` is not connected, use manual uploads
- If supporting evidence is incomplete, output as draft with blockers
- If verification is incomplete, mark as not final

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
