# Case Study 03 — Matrtix-Cleaner

Browser-side operator tooling for guarded bulk changes in OpenText approval matrices.

## Problem

Approval matrices are risky to edit manually.

The work is repetitive, but mistakes can have serious operational consequences:

- wrong signer;
- missing approver;
- incorrect legal entity binding;
- inconsistent document type rule;
- silent difference between rows that look similar;
- hard-to-review bulk changes.

The core problem was not just speed. The core problem was how to reduce manual effort without turning matrix editing into blind mass mutation.

## Solution

`Matrtix-Cleaner` is a Tampermonkey userscript that augments the existing OpenText interface.

Instead of replacing the system, it works inside the operator's existing browser workflow and adds a controlled layer around common matrix operations.

The tool is designed around:

- matrix inspection;
- planned changes;
- preview / dry-run thinking;
- scoped batch actions;
- ambiguity handling;
- operator review before applying changes.

This makes the project closer to an operator safety tool than to a raw DOM script.

## Stack

- JavaScript
- Tampermonkey
- Browser DOM integration
- jQuery / host-page context
- OpenText page structure and client-side objects

## Result

The project shows practical automation in an enterprise-like environment where clean APIs are not always available.

Key value:

- faster repeated matrix operations;
- better visibility before applying changes;
- reduced risk compared with manual row-by-row edits;
- a more structured operator workflow;
- reusable patterns for browser-side augmentation.

The project should be presented as a serious applied automation tool, not as a generic extension or toy script.

## What I learned

- Browser automation is often the most practical path when the real system does not expose a clean API.
- Safety rails matter more than raw speed when a script can change business-critical data.
- A good operator tool should make ambiguity visible instead of pretending every case is clean.
- Preview, audit, and bounded execution are what turn a script into a tool.

## Portfolio role

This is one of the strongest portfolio projects for workflow automation.

It is best used to show:

- practical enterprise automation;
- operator UX thinking;
- safe mutation design;
- JavaScript beyond frontend visuals;
- ability to work with imperfect existing systems.

## Related repository

- [`Matrtix-Cleaner`](https://github.com/ShapArt/Matrtix-Cleaner)
