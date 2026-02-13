# Belastingadviseur Plugin

A bilingual Dutch tax workflow plugin for [Cowork](https://claude.com/product/cowork) and Claude Code.
It supports full-spectrum Netherlands tax operations for **particulier, ZZP, and BV** use cases.

> **Important / Belangrijk**:
> This plugin supports tax workflows, not legal or fiscal advice.
> All outputs must be reviewed by a qualified Dutch tax professional before filing, payment, objection, or legal submission.

## Installation

This repository contains the plugin source at `belastingadviseur/`.

Install it through your Cowork/Claude plugin import flow using that folder.

If your local CLI version supports plugin install commands, use that version's
plugin install flow for `belastingadviseur/`.

## Commands

| Command | Description |
|---------|-------------|
| `/belastingadviseur:intake` | Intake and dossier setup for taxpayer profile, obligations, and missing documents |
| `/belastingadviseur:tax-calendar` | Build a verified tax deadline calendar for the selected year/profile |
| `/belastingadviseur:ib-aangifte` | Prepare inkomstenbelasting workflow (box 1/2/3 context, checks, and filing readiness) |
| `/belastingadviseur:btw-aangifte` | Prepare and check BTW return workflow for monthly/quarterly/annual obligations |
| `/belastingadviseur:vpb-aangifte` | Prepare vennootschapsbelasting workflow and pre-filing control checklist |
| `/belastingadviseur:loonheffingen` | Prepare payroll tax workflow (loonheffing, wage tax, social contributions, WKR checks) |
| `/belastingadviseur:aftrekcheck` | Validate relevant deductions, credits, and scheme eligibility with evidence checklist |
| `/belastingadviseur:bezwaar-brief` | Draft a Dutch bezwaar letter template with legal references and deadline controls |

## Skills

| Skill | Description |
|-------|-------------|
| `belasting-intake-en-dossiervorming` | Intake framework, document requests, taxpayer segmentation, and dossier quality controls |
| `inkomstenbelasting-boxen` | Box-based IB workflow (box 1/2/3), evidence mapping, and risk checks |
| `omzetbelasting-btw` | VAT period handling, output/input VAT checks, ICP logic, and correction flows |
| `vennootschapsbelasting-vpb` | Corporate tax workflow, fiscal profit bridge, and supporting schedules |
| `loonheffingen-en-werkkosten` | Payroll tax filing workflow including WKR, payroll evidence, and periodic controls |
| `aftrekposten-en-regelingen` | Deduction and allowance qualification workflow for individuals and businesses |
| `bezwaar-en-correspondentie` | Objection structure, argument mapping, and correspondence quality standards |
| `officiele-bronverificatie` | Mandatory verification protocol for rates, dates, thresholds, and legal references |

## Official Source Policy

This plugin enforces an official-source-first policy before any date/rate/threshold/legal claim:

1. Verify against `belastingdienst.nl` and/or `wetten.overheid.nl`.
2. Cite exact URL and retrieval date (`YYYY-MM-DD`) in output.
3. If verification is unavailable, explicitly mark the item as **not verified** and do not present it as final.

## Connectors

If placeholders like `~~boekhouding` or `~~data warehouse` appear, see [CONNECTORS.md](CONNECTORS.md).

## Example Workflows

### Yearly intake and planning

1. Run `/belastingadviseur:intake zzp 2025`.
2. Run `/belastingadviseur:tax-calendar 2025 zzp`.
3. Confirm missing documents and filing responsibilities.

### Periodic VAT cycle

1. Run `/belastingadviseur:btw-aangifte 2025-Q1 zzp`.
2. Validate input/output VAT evidence.
3. Track risks and follow-up actions before filing.

### Objection preparation

1. Run `/belastingadviseur:bezwaar-brief inkomstenbelasting 2026-02-05`.
2. Add assessment details and factual grounds.
3. Validate legal references and submission timing.

## Configuration

Edit `.mcp.json` to align with your connected stack.
Keep legal/tax authority verification on official Dutch sources only.
