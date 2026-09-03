# Case Notes

Short notes behind the public projects linked from my [GitHub profile](https://github.com/ShapArt).

The main profile stays intentionally compact. This repository keeps the extra context: **where a project came from, what is actually implemented, what result it produced, and what its limits are**. The linked repositories remain the source of truth for code and current documentation.

## Work-derived automation

| Project | Context | Result / focus |
|---|---|---|
| [OpenText Toolkit / Matrix Cleaner](cases/matrix-cleaner.md) | Cherkizovo · OpenText approval matrices | Guarded bulk edits, request parsing, preview/apply/rollback; covered mass changes went from hours to roughly 10 minutes |
| [TESSA Matrix Studio](cases/tessa-matrix-studio.md) | Cherkizovo · TESSA approval matrices | XLSX round-trip with row identity, exact diff, fresh-state checks and controlled apply |
| [Outlook SLA Toolkit](cases/outlook-sla-toolkit.md) | NAOS · Outlook-driven support workflow | Outlook COM → SQLite → SLA state → Excel/reminders; removed roughly an hour/day of repetitive work in covered tasks |

## Personal / academic projects

| Project | Context | Current scope |
|---|---|---|
| [EyeGate-L](cases/eyegate-l.md) | University engineering project | Two-door access-control prototype: FastAPI, camera/vision pipeline, gate FSM, auth, React UI and hardware-facing layer |
| [SH4PART VPN](cases/sh4part-vpn.md) | Self-hosted backend project | Telegram Stars payment state → SQLite → Hiddify provisioning → subscription delivery/reminders |

## Evidence outside these notes

- **Alfa CTF 2026 — 45th place**
- **VK Education — Application Security / AppSec**, 2025
- **BMSTU Digital Department — Web Developer**, 2024
- Stepik certificates in DevOps, cyberattack countermeasures, trusted AI, SQL, hardware security and probability
- Skolkovo / Arctic Probe engineering-project winner, 2020

The current certificate/evidence index lives in the profile repository: [CERTIFICATES.md](https://github.com/ShapArt/ShapArt/blob/main/CERTIFICATES.md).

## About internal work

The OpenText/TESSA notes describe the engineering shape of the work without publishing credentials, private documents, employee data or non-public configuration. Public code and examples use synthetic or non-sensitive data where required.

## По-русски

Здесь лежит дополнительный контекст к проектам из основного GitHub-профиля. Не «почему этот проект крутой» и не самооценка, а факты: откуда появилась задача, что реально сделано, какой получился результат и где заканчивается область применимости.

Основные рабочие кейсы сейчас — **OpenText Toolkit / Matrix Cleaner** и **TESSA Matrix Studio**. Outlook SLA Toolkit показывает предыдущую рабочую автоматизацию; EyeGate-L и SH4PART VPN — отдельные технические проекты.
