![Claude AI voor Belastingdienst](belastingadviseur_banner.png)

# Belastingadviseur Plugin

A bilingual Dutch tax workflow plugin for [Cowork](https://claude.com/product/cowork) and Claude Code.
It supports full-spectrum Netherlands tax operations for **particulier, ZZP, and BV** use cases.

> **Important / Belangrijk**:
> This plugin supports tax workflows, not legal or fiscal advice.
> All outputs must be reviewed by a qualified Dutch tax professional before filing, payment, objection, or legal submission.

## Installation

Install through the Cowork or Claude Code plugin import flow, pointing at the root of this repository.

Pre-built zip files are also available on the [GitHub Releases](../../releases) page — download one and use the "upload plugin" option in the import flow.

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

## Testdata

De map `testdata/` bevat dummy CSV-bestanden om de plugin mee te testen.

| Bestand | Klant | Te testen met |
|---------|-------|---------------|
| `klanten.csv` | Alle 5 klanten | `/belastingadviseur:intake` — klantprofielen voor zzp, bv en particulier |
| `zzp_jan_boekhouding_2025.csv` | Jan de Vries (ZZP) | `/belastingadviseur:ib-aangifte`, `/belastingadviseur:btw-aangifte`, `/belastingadviseur:aftrekcheck` |
| `zzp_pieter_btw_q2_2025.csv` | Pieter Bakker (ZZP) | `/belastingadviseur:btw-aangifte` — bevat ICP (DE, BE, CH), verlegd en openstaande facturen |
| `bv_broodjes_resultatenrekening_2025.csv` | Bakkerij Broodjes BV | `/belastingadviseur:vpb-aangifte` — volledige resultatenrekening voor fiscale winstbepaling |
| `bv_broodjes_btw_q1_2025.csv` | Bakkerij Broodjes BV | `/belastingadviseur:btw-aangifte` — Q1 verkoop- en inkoopfacturen met ICP-inkoop |
| `bv_broodjes_loonheffingen_2025_jan.csv` | Bakkerij Broodjes BV | `/belastingadviseur:loonheffingen` — 8 werknemers, diverse contractvormen en WKR |
| `particulier_maria_inkomsten_2025.csv` | Maria Jansen (particulier) | `/belastingadviseur:ib-aangifte` — salaris, eigen woning, fiscaal partner, giften |
| `particulier_maria_box3_2025.csv` | Maria Jansen (particulier) | `/belastingadviseur:ib-aangifte` — box 3 vermogen incl. crypto en tweede woning |

## Configuration

Edit `.mcp.json` to align with your connected stack.
Keep legal/tax authority verification on official Dutch sources only.
