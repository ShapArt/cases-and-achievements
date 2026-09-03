# SH4PART VPN

**Small self-hosted backend connecting Telegram Stars payment state to VPN subscription provisioning.**

Repository: [ShapArt/vpn-bot-stars-hiddify](https://github.com/ShapArt/vpn-bot-stars-hiddify)

## Context

The useful part of a subscription bot is not the `/start` screen. The real workflow crosses several systems: payment confirmation, local entitlement/order state, external provisioning and delivery of usable subscription data back to the user.

## Built

The service is a compact FastAPI application with this path:

```text
Telegram user
    ↓
plan / Stars invoice
    ↓
pre-checkout + successful payment
    ↓
SQLite user/order state
    ↓
Hiddify provisioning
    ↓
subscription URL / QR / onboarding
    ↓
expiry reminders / renewal
```

The repository includes:

- Telegram webhook handling;
- Telegram Stars payment events;
- SQLite users, orders and reminder idempotency state;
- configurable plans through environment JSON;
- Hiddify provisioning through direct, bridge or external-command paths;
- subscription link/onboarding output;
- APScheduler expiry reminders;
- environment-driven secrets and deployment settings.

## Current scope

This is a small self-hosted service, not a full billing platform. Most runtime logic intentionally remains in one `app/main.py`, which keeps the end-to-end flow easy to trace but would be a natural split point if the service became much larger.

## Constraints

- Production Telegram flow requires a public webhook endpoint.
- Telegram/Hiddify credentials are deployment secrets and are not stored in the repository.
- SQLite is a pragmatic choice for this deployment size, not a claim of horizontally scalable billing architecture.
- Provisioning reliability still depends on the configured external Hiddify path.

## Evidence

- [Project README](https://github.com/ShapArt/vpn-bot-stars-hiddify)
- [`app/main.py`](https://github.com/ShapArt/vpn-bot-stars-hiddify/blob/main/app/main.py)
- [`.env.example`](https://github.com/ShapArt/vpn-bot-stars-hiddify/blob/main/.env.example)
