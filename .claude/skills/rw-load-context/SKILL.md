---
name: rw-load-context
description: Step 1b of regulation watch. Read the context index, the product card, the relevant control cards and sources.md before gathering or writing anything. Use at the start of every regulation watch run and again before writing the table.
---

# Load context

Inputs: `CLAUDE.md`, the date window.

## Before gathering

1. Read `context/index.md`. Note which cards exist, how far to trust them, and the known gaps.
2. Read `context/product/close-management-ai-features.md` every run.
3. Read `sources.md` (allowed sources and minimum fetches).
4. Build a watch list from the product card's "Watch for" section. Use it to choose search terms and which linked pages to open in `rw-gather`. It guides what to look for, never what to conclude.

## Before assessing and writing

For each in-window item:

1. Use the index's "Open when" column to pick the control cards that match the item, and read those cards, including their "Watch for". Read each at most once per run.
2. If none matches, say so in the row ("no control card matched").

## Rules

- Cards are context, not evidence. A regulatory claim needs an official page fetched in this run. A card line supplies "which feature and why" and "what to check first", and the row names the card it came from (for example "product card" or "sample control AI-02").
- Control cards are SAMPLE DATA. Say "sample control AI-0x". Never state that FloQast operates, passes or fails a control.
- Lines marked **confirm** and the index's known gaps are unknown, not "no". If an item depends on one, add it to the gaps list as "Unconfirmed: ...".
- If a card conflicts with `CLAUDE.md` product facts, use `CLAUDE.md` for the run and list the conflict in the gaps.
- Do not write anything to the context files during a run.
