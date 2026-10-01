# CDL-bibliography-stacks

This repository is an **archive**. It holds the working records from the September 2026 verification of the Contextual Dynamics Lab's shared bibliography, [ContextLab/CDL-bibliography](https://github.com/ContextLab/CDL-bibliography). It is not maintained, and it is not where the bibliography or its tools live.

**Looking for the bibliography (`cdl.bib`) or the `bibcheck` tool?** Use [ContextLab/CDL-bibliography](https://github.com/ContextLab/CDL-bibliography). The copies of `cdl.bib`, `bibcheck/` and the tests in this repository are a frozen snapshot from 2026-09-30 (CDL-bibliography commit `338b520`). They are out of date and should not be used or cited from here.

## Why this exists

Between September 9 and 30, 2026, every entry in `cdl.bib` was checked against its published record. That work produced about 1,400 files (around 143 MB) of intermediate records: research notes, batch inputs and outputs, review pages, audits and earlier baselines. CDL-bibliography itself keeps only what the tool needs: the library, the checker, its tests, and the saved verification results with their evidence (`verification/baseline.jsonl.gz`). These records were moved here so the main repository stays small, while the full audit trail stays public. The decision log and design notes in CDL-bibliography link to files here.

## What's in `verification/`

Folders are named by the date they were created.

| Records | Folders |
|-|-|
| First Crossref pass, automatic review, early follow-ups | `automatic-review.md`, `incremental-verification-2026-09-14.md`, `resolution-2026-09-15/`, `resolution-followup-2026-09-15/`, `completion-2026-09-15/`, `pilot50/`, `benchmark/`, `HANDOFF-2026-09-11.md` |
| Rules, plans and new sources | `resolution-plan-2026-09-22/` (the decision log as it stood then), `phase0-2026-09-22/`, `catalogue-phase0-2026-09-22/`, `extra-sources-2026-09-23/`, `spotcheck-2026-09-23/`, `fixes-2026-09-24/`, `routes-2026-09-25/`, `machinery-2026-09-25/`, `pr-check-2026-09-25/` |
| Research waves (entries no automatic source could settle, researched one at a time, each field matched to a quoted source) | `research-pilot-2026-09-24/`, `research-2026-09-25/` (waves 1-9 and the cross-wave decisions), `research-2026-09-26-manual/`, `resolution-2026-09-26/`, `resolution-2026-09-27/`, `research-route-2026-09-27/` |
| Applying the results (each batch applied, re-verified and tested before it was committed) | `apply-2026-09-23/` through `apply-2026-09-30d-followup/` |
| Review pages and the user's answers | `2026-09-29-user-review/`, `2026-09-30-user-review/` |
| Snapshots and logs | `baseline.jsonl.gz`, `baseline-policy1.jsonl.gz`, `baseline-in-progress.jsonl.gz`, `auto-reviewed.jsonl.gz`, `review-queue.jsonl.gz`, `key-renames.json`, `key-deletions.json`, `revocations.jsonl`, `journal-alias-audit-2026-09-26.json` |
| One-off scripts | `dartmouth_pilot.py`, `discovery_pilot.py`, `incremental_pilot.py`, `neurips_record_lookup.py`, `pdf-benchmark/` |

`verification/README.md` (from 2026-09-30) maps the old folder names to the current ones.

The `crossref research-approve` command and the tests that read these folders exist only in this snapshot; CDL-bibliography removed them when the records moved here.
