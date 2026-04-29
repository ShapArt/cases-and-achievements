# Case Study 02 — SLA / Outlook Tracker

Office automation and reporting workflow for turning mailbox-driven operational work into structured data.

## Problem

A lot of operational work lives in email: requests, follow-ups, status updates, deadlines, responsibility changes, and confirmations.

When that information stays only inside Outlook, the workflow becomes fragile:

- statuses are hard to track consistently;
- repeated manual checks waste time;
- Excel reports are rebuilt by hand;
- overdue items are easy to miss;
- the process depends too much on memory and manual discipline.

The problem was to make mailbox-driven work more structured and easier to review.

## Solution

The project direction is a Windows-first Outlook export and tracking workspace.

The system extracts or processes Outlook-derived data and moves it toward a structured workflow:

- collect relevant mailbox items;
- normalize message fields and dates;
- store or prepare operational records;
- export data into spreadsheet-friendly formats;
- support status tracking and follow-up workflows;
- reduce repeated manual copy-paste.

The goal is not to replace Outlook. The goal is to turn Outlook into a better input source for operational control.

## Stack

- Python
- pywin32 for Outlook integration
- pandas for tabular processing
- openpyxl for Excel-compatible output
- PySide6 for desktop/UI-oriented tooling
- SQLite-style local state direction

## Result

The value of this project is practical:

- less manual handling of mailbox data;
- clearer status tracking;
- better reporting structure;
- more repeatable export workflow;
- stronger basis for SLA-style monitoring.

This is a strong business-facing project because the problem is immediately understandable even to non-developers: less manual tracking, fewer missed statuses, better visibility.

## What I learned

- Office automation is real engineering when it touches messy data, local environments, and human workflows.
- Outlook and Excel are not “boring tools” — they are often where operational truth lives.
- Good automation should fit into the operator's existing workflow instead of forcing a completely new system too early.
- A small export tool can have high value if it removes repeated manual work.

## Portfolio role

This project is important because it shows applied automation in a business context.

It is best used to show:

- Python automation;
- Windows / Outlook integration;
- spreadsheet and reporting workflows;
- operator-oriented thinking;
- practical value beyond toy examples.

## Related repository

- [`outlook-exporter`](https://github.com/ShapArt/outlook-exporter)
