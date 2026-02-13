---
description: Build verified Dutch tax filing calendar
argument-hint: "<belastingjaar> [profieltype]"
---

# Tax Calendar / Belastingkalender

> If placeholders are unclear, see [CONNECTORS.md](../CONNECTORS.md).

**Important / Belangrijk**: This workflow support is not legal or fiscal advice. Require review by a qualified Dutch tax professional.

Create a tax deadline calendar for Dutch obligations with official-source verification.

## Usage

```bash
/belastingadviseur:tax-calendar <belastingjaar> [profieltype]
```

## Workflow

1. Determine scope:
- Year and profile (`particulier`, `zzp`, `bv`)
- Filing frequencies (monthly/quarterly/annual)

2. Determine obligation set:
- Include only applicable categories (IB, BTW, VPB, loonheffingen, and related tasks)
- Label optional vs mandatory milestones

3. Verify every deadline:
- Check `belastingdienst.nl` for operational deadlines and filing windows
- Check `wetten.overheid.nl` when legal timing basis must be cited
- Record verification URL and retrieval date for each date-sensitive claim

4. Build practical planning layer:
- Add internal buffer dates (prep/review/sign-off)
- Flag dependencies on external data and approvals

5. Fallback behavior:
- If no connectors are available, produce the same calendar with explicit assumptions and manual document requirements
- If official source cannot be verified, mark item as unverified and do not present as final

## Required Output Format (Use Exactly)

1. `Context / Context`
2. `Assumptions / Aannames`
3. `Required Documents / Benodigde stukken`
4. `Step-by-step / Stappenplan`
5. `Checks & Risks / Controles en risico's`
6. `Next Actions / Volgende acties`
7. `Sources (official) / Bronnen (officieel)`
8. `Professional Review Disclaimer / Disclaimer deskundige beoordeling`
