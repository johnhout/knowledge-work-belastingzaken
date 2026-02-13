---
name: officiele-bronverificatie
description: This skill should be used whenever outputs depend on Dutch tax rates, thresholds, dates, filing deadlines, legal references, or procedural requirements. Trigger phrases include "check official source", "verifieer met Belastingdienst", "is dit nog actueel", "latest Dutch tax deadline", and "wettelijke bron".
---

# Officiele Bronverificatie

Use this skill as the mandatory verification layer for all rule-sensitive tax outputs.

## Scope

- Source validation for rates, thresholds, deadlines, and procedural rules
- Legal citation validation for statutory references
- Freshness checks with retrieval-date logging

## Boundaries

- Only treat `belastingdienst.nl` and `wetten.overheid.nl` as authoritative.
- Do not elevate third-party summaries above official sources.
- Do not present stale or unverifiable claims as final guidance.

## Verification Protocol

1. Identify each claim that is date/rate/rule dependent.
2. Verify practical guidance and deadlines on `belastingdienst.nl`.
3. Verify legal basis text on `wetten.overheid.nl` where applicable.
4. Capture exact URL, page topic, and retrieval date (`YYYY-MM-DD`).
5. If source conflict exists, report conflict explicitly and require professional review.
6. If source unavailable, mark claim as unverified and stop short of definitive guidance.

## Escalation Points

Escalate when:
- Official sources appear to conflict
- No current source confirms a high-impact claim
- Filing or objection timing is near and unresolved

## Safety

This skill enforces quality and recency controls; it does not replace professional legal or fiscal advice.
