---
description: Prepare inkomstenbelasting workflow and checks
argument-hint: "<belastingjaar> [profieltype]"
---

# IB Aangifte / Income Tax Filing

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Prepare Dutch income tax workflow for individuals and entrepreneurs (where applicable), including box-based checks.

## Usage

```bash
/belastingadviseur:ib-aangifte <belastingjaar> [profieltype]
```

## Workflow

1. Intake IB context:
- Household situation, income sources, business income relevance
- Prior-year carryforwards and known open issues

2. Structure by box:
- Box 1: work/home and taxable income components
- Box 2: substantial interest context where relevant
- Box 3: assets/liabilities and evidence requirements

3. Gather support:
- Statements, annual overviews, expense support, prior assessments
- Reconcile user-provided figures against source evidence

4. Apply checks and controls:
- Completeness checks per box
- Consistency checks against prior periods
- Material variance flags and data quality exceptions

5. Official-source verification:
- Verify thresholds, rates, deadlines, and formal criteria on `belastingdienst.nl`
- Verify legal basis references on `wetten.overheid.nl`
- Include URL and retrieval date for each rule-dependent claim

6. Fallback behavior:
- If `~~boekhouding` or `~~data warehouse` is not connected, continue with manual evidence and mark assumptions
- If a rule cannot be verified officially, mark as unverified and require professional confirmation

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
