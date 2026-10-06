---
doc: scope
status: draft
---
# Shift Handoff
A browser-only tool that turns a shift lead's rough notes into a clear next-shift handoff.

## The Unique Kernel
It never hides what is unfinished. Notes become proposed tasks and incidents, and anything without an owner or a date is flagged in the exported handoff instead of silently dropped.

## Who It's For
A shift lead at a small shop (a cafe, a retail store, a small kitchen). Today they leave a text, a sticky note, or a verbal rundown, and things get lost between shifts.

## The Core Loop
End of shift: paste notes, review the proposed tasks and incidents, assign owners and dates, export the handoff for the next shift.

## Inspiration & Identity
Plain, fast, low-friction. Closer to a clipboard than a project-management tool. Warning colors only for gaps.

## Why This Matters to the Learner
Not established. The learner delegated the planning decisions ("You decide"); the choices below are recorded assumptions, listed in `docs/assumptions.md`.

## What "Working" Looks Like
Pasting three lines of notes yields three editable items. Leaving one without an owner or date highlights it, and the exported handoff marks it "NEEDS ATTENTION" under a warning line that counts the gaps.

## The POC Boundary
- Paste notes, one line per item; a leading "!" or "incident:" marks an incident.
- Review and edit proposed items, add or remove items.
- Assign owner and date.
- Export a text handoff, copy to clipboard.
- Everything local to the browser.

## Later
Photos on incidents, recurring tasks, multiple shift leads, sharing links.

## Explicitly Cut
- Accounts and sync: a POC needs no backend and nothing private leaves the device.
- AI parsing of free-form notes: adds a key and cost; the one-line rule is enough to prove the loop.
- Notifications: out of scope for a single-device loop.
