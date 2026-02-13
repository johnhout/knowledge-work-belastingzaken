---
description: Draft bezwaar letter with deadlines and evidence
argument-hint: "<onderwerp> [beschikkingdatum]"
---

# Bezwaar Brief / Objection Letter

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Draft a structured bezwaar letter template for Dutch tax correspondence.

## Usage

```bash
/belastingadviseur:bezwaar-brief <onderwerp> [beschikkingdatum]
```

## Workflow

1. Intake objection context:
- Decision/assessment type and reference number
- Date of assessment and objection timing context
- Factual background and requested remedy

2. Build argument structure:
- Facts and chronology
- Disputed points and supporting evidence
- Requested correction or relief

3. Legal and procedural checks:
- Verify objection windows and procedural requirements on `belastingdienst.nl`
- Verify article references and legal basis on `wetten.overheid.nl`
- Capture exact URL + retrieval date

4. Draft correspondence package:
- Formal letter structure in Dutch with optional English summary
- Evidence checklist and annex references
- Submission checklist and follow-up timeline

5. Fallback behavior:
- If source documents are incomplete, produce a draft with explicit missing inputs
- If legal basis cannot be officially verified, mark argument as pending verification
- Escalate complex or high-stakes objections to a qualified advisor

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
