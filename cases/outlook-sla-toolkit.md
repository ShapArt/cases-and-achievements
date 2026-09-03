# Outlook SLA Toolkit

**Windows automation around an Outlook-driven support workflow.**

Repository: [ShapArt/outlook-exporter](https://github.com/ShapArt/outlook-exporter)

## Context

At NAOS, part of the support workflow lived across Outlook messages, manual status tracking and Excel. Repeated checks and copy-paste made it easy for deadlines and current state to depend on individual memory.

## Built

The project grew from a mail export utility into a small local operations tool:

```text
Classic Outlook / MAPI
        ↓
message ingest + sender/customer extraction
        ↓
SQLite ticket state
        ↓
SLA/status calculation
        ├──→ Excel export / reviewed sync
        └──→ overdue plan / reminders
```

The current code includes:

- Classic Outlook COM/MAPI integration through `pywin32`;
- customer/sender extraction and configurable sender filtering;
- ticket/status and business-hour SLA logic;
- SQLite persistence;
- Excel export and round-trip synchronisation;
- overdue reminder planning/sending;
- PySide6 desktop UI;
- CLI diagnostics and QA/semi-E2E commands;
- pytest coverage for SLA, filters, status mapping, DB and Excel workflows.

## Result

In the workflow it was built for, the automation removed roughly **an hour of repetitive work per day** across covered tasks and made overdue requests easier to see and follow up.

## Constraints

- The direct mail integration requires **Windows + Classic Outlook** because it uses COM/MAPI.
- New Outlook does not provide the same COM path; the tool diagnoses this explicitly.
- Mail sending can be disabled separately from reading/processing.
- Safe mode and allowlists are available for QA/test runs.
- SQLite is appropriate for the local workflow; the project is not presented as a distributed ticketing platform.

## Evidence

- [Project README](https://github.com/ShapArt/outlook-exporter)
- [`core/outlook.py`](https://github.com/ShapArt/outlook-exporter/blob/main/core/outlook.py)
- [`core/sla.py`](https://github.com/ShapArt/outlook-exporter/blob/main/core/sla.py)
- [Tests](https://github.com/ShapArt/outlook-exporter/tree/main/tests)
