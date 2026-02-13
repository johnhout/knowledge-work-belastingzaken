# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category.
This plugin is tool-agnostic and uses categories instead of fixed vendors.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|------------------|---------------|
| Boekhouding / Accounting | `~~boekhouding` | -- | Exact Online, Twinfield, QuickBooks, Xero |
| Salarisadministratie / Payroll admin | `~~salarisadministratie` | -- | Loket.nl, Nmbrs, AFAS |
| Documentopslag / Document storage | `~~documentopslag` | Microsoft 365 (SharePoint/OneDrive), Notion | Box, Google Drive, Dropbox |
| Email | `~~email` | Microsoft 365 | Gmail |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Data warehouse | `~~data warehouse` | BigQuery, Snowflake* | Databricks, Redshift, PostgreSQL |

\* Placeholder - MCP URL not yet configured.
