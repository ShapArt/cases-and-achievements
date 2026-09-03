# OpenText Toolkit / Matrix Cleaner

**Work-derived operator tooling for OpenText approval matrices.**

Repository: [ShapArt/Matrtix-Cleaner](https://github.com/ShapArt/Matrtix-Cleaner)

## Context

At Cherkizovo, approval matrices contain routing rules for approvers and signers across legal entities, sites, categories, functions, document types, amount ranges and other conditions.

Large requests are repetitive to execute row by row, but the rows are not interchangeable: similar-looking entries can have different scope. Speed without review would make bulk editing more dangerous, not less.

## Built

OpenText Toolkit is a Tampermonkey panel that works on top of the existing OpenText/ITSM pages. The current repository includes:

- signer and approver operations;
- card-attribute changes;
- request parsing into a proposed plan;
- route/card diagnostics;
- matrix reconciliation and summary work;
- multi-step builder flows;
- Excel round-trip for bulk editing;
- rollback within the current session;
- Playwright and regression/evaluation suites built around real failure modes.

The main write path is intentionally plan-based:

```text
request / operator input
        ↓
inspect current matrix
        ↓
build explicit plan
        ↓
preview affected rows
        ↓
operator review
        ↓
re-check row fingerprints
        ↓
apply to page model
        ↓
operator uses OpenText's normal save action
```

The userscript does **not** press OpenText's final save button on behalf of the operator.

## Result

For typical covered mass-change scenarios, work that previously took hours of repetitive UI editing can be prepared and completed in roughly **10 minutes**.

The tool is used in day-to-day OpenText work by me and a senior specialist.

## Constraints

- It does not grant or elevate OpenText permissions.
- Ambiguous people/categories/scope are treated as ambiguity rather than guessed matches.
- A broad plan without narrowing conditions requires explicit confirmation.
- Fresh row fingerprints are checked before applying a reviewed plan.
- The repository documents known limitations separately instead of presenting the tool as universally safe.

## Evidence

The public repository contains a synthetic demo page, screenshots, known limitations, regression suites and the installable userscript:

- [README](https://github.com/ShapArt/Matrtix-Cleaner)
- [Known limitations](https://github.com/ShapArt/Matrtix-Cleaner/blob/main/KNOWN_LIMITATIONS.md)
- [Demo](https://github.com/ShapArt/Matrtix-Cleaner/blob/main/docs/demo/matrix-demo.html)
