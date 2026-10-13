---
name: rw-render-verify
description: Steps 6 to 8 of regulation watch. Add null rows, render the table, gaps list and three first actions, and run the verification checklist. Use after rw-assess and before sending the answer.
---

# Null check, render, verify

## Null rows

For every source with nothing in the window, add a row "No in-window item found" with the page and date checked. Never omit a source.

## Format

1. One table, columns: `# | Item (page link, date) | What it requires | Feature touched and why | Impact (High/Medium/Low + reason) | Key dates | First thing to check | Owner`. Cells concise. Link text names the page; the date goes in the same cell. Order: High, Medium, Low; within a level, by earliest key date. Null rows go last. Owner is "TBC" unless supplied.
2. **What I could not source or confirm**: bullets. Always include: UK coverage; any primary text not opened; owners left TBC; any page that failed to load; every "Unconfirmed:" item; the context-index gaps the rows depend on; and a note that control mappings are sample data.
3. **Do these first**: exactly three numbered lines, each an action with a date or owner if known, ordered by urgency (nearest deadline or already-enforceable first).

No emojis. Keep it concise.

## Verify before sending

- Every row has a page link and a date.
- Every claim traces to a page fetched this run.
- No "would" or "likely" stated as fact; judgments marked "my reading".
- All five sources appear in the table or gaps.
- The gaps list matches what was actually not read.
- Exactly three "do these first" lines.
- Context was read before writing: index, product card, `sources.md`, and the matched control cards. Each row names the card behind its feature or control judgment, or says no control card matched.
- Control cards are called "sample control AI-0x", never FloQast's operating controls.
- No regulatory claim rests on a card; each rests on an official page fetched this run.
- Every "confirm" or known-gap item an included row depends on is in the gaps list.
- On a re-run with unchanged sources, structure, order, ratings and gaps are identical; if a page changed, say which and its new date.
