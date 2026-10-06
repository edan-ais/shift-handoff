---
doc: prd
status: draft
---
# Shift Handoff - Product Requirements
A single page where a shift lead turns pasted notes into an assigned, flagged next-shift handoff.
Source: `scope.md > The Core Loop`, `scope.md > The POC Boundary`.

## The Core Journey
1. Open the page. An empty notes box and an empty review list appear.
2. Paste or type notes, one item per line. Lines starting with "!" or "incident:" are incidents.
3. Press "Propose tasks". Each line becomes an editable item typed Task or Incident.
4. Edit text, switch type, enter an owner, pick a date, or delete items.
5. Items missing an owner or date are highlighted.
6. Press "Build handoff". A text handoff appears, grouped into Incidents and Tasks, with a gap count and "NEEDS ATTENTION" on gaps.
7. Press "Copy" to paste it into a message or chat.
Success: the lead sends the handoff and nothing unfinished is hidden.

## Screens and Layout
One page, top to bottom: notes box, review list, handoff output.

## Look and Feel
Plain system font, narrow single column, light background. Yellow highlight for items with gaps, red text only for incident-type context.

## Features and Behavior
- As a shift lead, I want to paste notes and get items so that I do not retype them.
  - [ ] Three non-empty lines produce three items.
  - [ ] Blank lines are ignored.
  - [ ] "!" and "incident:" prefixes create incidents with the prefix removed.
- As a shift lead, I want gaps flagged so that nothing is left ownerless.
  - [ ] An item without owner or date shows a highlight.
  - [ ] The highlight clears when both are filled.
  - [ ] The export lists UNASSIGNED / NO DATE and a gap count.

## States and Boundaries
- **First use** - empty list; export shows "- none" for both groups.
- **Persistence** - items persist in the browser (localStorage) across reloads; "Clear" removes them.
- **Privacy** - no network calls, no accounts.

## Product Decisions
- First user is a shift lead (assumed; learner said "You decide").
- Scope is tasks plus incidents, small first scope (assumed).
- Export allowed with gaps, clearly flagged (assumed).

## What We're Building
Everything in the core journey above.

## Deferred From the POC
Sharing, accounts, recurring tasks, photos: each needs a backend or more design than a POC warrants.

## Non-Goals
No AI parsing, no notifications, no multi-user editing.

## Open Questions
None blocking. The learner may revisit the assumed choices.
