# TESSA Matrix Studio

**Excel round-trip editor for TESSA approval matrices.**

Repository: [ShapArt/tessa-matrix-studio](https://github.com/ShapArt/tessa-matrix-studio)

## Context

Large TESSA matrices are much easier to edit as structured tabular data than through many individual UI operations. The risky part is the return trip: an Excel row must still refer to the same live matrix row that was reviewed before anything is written back.

## Built

TESSA Matrix Studio adds an operator panel to an open matrix and uses this workflow:

```text
TESSA
  ↓
structured XLSX export
  ↓
bulk Excel edits
  ↓
exact diff / operation plan
  ↓
operator review
  ↓
fresh live-state validation
  ↓
controlled apply
  ↓
optional result verification
```

The workbook carries hidden identity/baseline information. Studio distinguishes changes to existing rows from additions, replacements and deletions and blocks files whose structure or identity data cannot be trusted.

The project also includes diagnostics, release artifacts, regression tests, CodeQL and production/UAT documentation.

## Safety model

- Preview is read-only.
- Formula-bearing or structurally unsafe editable cells are rejected.
- A workbook exported from another matrix is blocked.
- Current matrix state is read again before Apply.
- Conflicting/unsafe operations are skipped instead of silently forced.
- Result verification is separate from successful completion of the write operation.
- Studio uses the current TESSA session and does not grant additional rights.

## Current state

The project is actively versioned and shipped as a Tampermonkey userscript. Its README keeps a known `LeftOperandExtractor` limitation visible rather than hiding it behind the installation flow.

## Evidence

- [Project README](https://github.com/ShapArt/tessa-matrix-studio)
- [Architecture](https://github.com/ShapArt/tessa-matrix-studio/blob/main/docs/ARCHITECTURE.md)
- [Production runbook](https://github.com/ShapArt/tessa-matrix-studio/blob/main/docs/PRODUCTION-RUNBOOK.md)
- [Releases](https://github.com/ShapArt/tessa-matrix-studio/releases)
