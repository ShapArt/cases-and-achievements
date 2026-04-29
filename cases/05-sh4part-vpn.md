# Case Study 05 — Sh4pArt VPN

Telegram-first VPN subscription backend with provisioning, profile delivery, and reminder logic.

## Problem

Small VPN subscription services often break at the handoff points:

- payment is separate from provisioning;
- keys are issued manually;
- users do not understand how to import profiles;
- subscription links and QR codes are delivered inconsistently;
- expiry reminders become manual support work;
- infrastructure details are easy to keep outside the product flow.

The problem was to connect service delivery into one predictable flow.

## Solution

`Sh4pArt VPN` is structured as a Telegram-first backend around the full delivery path:

1. user enters the bot;
2. user selects or pays for a plan;
3. backend provisions or refreshes access;
4. local state is stored;
5. the bot delivers subscription artifacts;
6. reminder logic handles future expiry windows.

The interesting part is the complete lifecycle, not just the Telegram interface.

## Stack

- Python
- FastAPI
- Telegram Bot API / Aiogram-style bot flow
- SQLite
- APScheduler
- Hiddify-oriented provisioning path
- Linux service / self-hosting direction
- nginx / TLS / iptables-style infrastructure basics

## Result

The project demonstrates a full-flow backend service:

- bot UX;
- API/webhook handling;
- persistent user/order state;
- provisioning integration;
- onboarding output with links / QR / deeplink style delivery;
- reminder scheduling;
- infrastructure-minded deployment thinking.

It is a strong portfolio project because it connects backend, infrastructure, and user-facing delivery.

## What I learned

- A bot becomes much more interesting when it owns a full service lifecycle.
- Provisioning and onboarding should be treated as part of the product, not as manual afterthoughts.
- Environment-driven configuration is critical for self-hosted services.
- SQLite can be a pragmatic choice for small deployments, but it should be documented as a trade-off.
- Good backend work is often about connecting boring steps reliably.

## Portfolio role

This is a strong backend/infrastructure case.

It is best used to show:

- FastAPI service design;
- Telegram bot backend work;
- provisioning flow thinking;
- self-hosted service delivery;
- practical operational engineering.

## Related repository

- [`vpn-bot-stars-hiddify`](https://github.com/ShapArt/vpn-bot-stars-hiddify)
