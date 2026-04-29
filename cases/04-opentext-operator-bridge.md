# Case Study 04 — OpenText Operator Bridge

Backend and operator workflow layer for fragmented OpenText-related support scenarios.

## Problem

Operational support work around document workflow systems rarely arrives in a clean form.

A request can be spread across:

- emails;
- forwarded messages;
- local files;
- portal pages;
- screenshots;
- incomplete descriptions;
- context that only the operator knows.

When the inputs are fragmented, automation becomes risky. A system should not jump straight from intake to action without diagnosis and review.

## Solution

`OpenText Operator Bridge` is designed as a backend and operator-facing workflow layer.

The project direction is to collect scattered operational inputs and turn them into a more controlled process:

- intake material from different sources;
- normalize files and messages;
- extract relevant entities;
- classify and diagnose cases;
- show queue / ticket views;
- prepare bounded next steps;
- keep human review in the loop where needed.

The important design principle is **guarded automation**: the tool should help operators move faster, but not hide risky decisions behind a magic button.

## Stack

- Python
- FastAPI
- SQLAlchemy
- Alembic-style database evolution
- Playwright for portal/browser automation
- pywin32 for Outlook / Windows integration
- server-rendered UI direction
- environment-driven configuration

## Result

The project shows a more mature kind of backend work than a typical CRUD demo.

It demonstrates:

- workflow orchestration;
- intake and triage thinking;
- integration with messy sources;
- environment-specific adapter design;
- operator-facing visibility;
- safe boundaries around automation.

This project is especially relevant to document workflow automation work because it connects backend systems with real operational constraints.

## What I learned

- The hardest part of automation is often not writing the action, but understanding the input correctly.
- Human review is not a failure of automation; sometimes it is the correct control boundary.
- Environment-specific integrations should be documented honestly instead of pretending everything is portable.
- Internal tools need UX, not only backend endpoints.

## Portfolio role

This is a flagship workflow/backend case.

It is best used to show:

- backend architecture around operations;
- document workflow automation thinking;
- Python/FastAPI skills;
- integration-heavy engineering;
- safe automation patterns.

## Related repository

- [`opentext-operator-bridge`](https://github.com/ShapArt/opentext-operator-bridge)
