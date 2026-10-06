---
doc: spec
status: draft
---
# Shift Handoff - Technical Spec

## How This Works, In Plain Language
One HTML file with inline CSS and JavaScript. Pasted notes are split by line into items kept in a JavaScript array and mirrored to localStorage. The handoff text is built from that array.

## The Core Journey Through the System
Notes textarea -> parse lines -> items array (type, text, owner, due) -> render rows -> export builds text from the array -> clipboard.

## Stack
Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies.

## Where It Runs and How Someone Tries It
Open `index.html` in any modern browser, or open the GitHub Pages / hosted copy if one is published. No install, no keys.

## Look and Feel
As in `prd.md > Look and Feel`: system font, 820px column, yellow row highlight for gaps.

## Components
### Parser
Splits notes on newlines, trims, drops blanks, sets type from a leading "!" or "incident:" (case-insensitive).
### Review list
One row per item with type select, text, owner, date and delete. The gap highlight toggles live as owner and date change.
### Exporter
Builds "SHIFT HANDOFF <date>", a gap warning when any item lacks an owner or date, then INCIDENTS and TASKS. Copy uses the clipboard API.

## Data Model
`items[]`: `{ type: "task" | "incident", text: string, owner: string, due: "YYYY-MM-DD" | "" }`, stored under localStorage key `sh_items`.

## File Structure
`index.html`, `README.md`, `devpost/` planning docs, `docs/assumptions.md`.

## External Services and Dependencies
None.

## Important Failure Modes
- Clipboard API unavailable: copy does nothing; the text is still selectable in the output box.
- localStorage disabled: items work for the session but do not persist.

## What Was Simplified and Why
Free-form notes are parsed by line, not by AI, to avoid keys, cost and a backend.

## Decisions and Open Issues
Assumed choices are recorded in `docs/assumptions.md`. No blocking issues.
