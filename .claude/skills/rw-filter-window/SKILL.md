---
name: rw-filter-window
description: Step 3 of regulation watch. Filter gathered items to those published or changed inside the date window. Use after rw-gather.
---

# Filter to the window

Inputs: the raw list from `rw-gather`, `window_start`, `window_end`.

1. Keep an item only if its published or changed date is inside the window (inclusive).
2. Record the date used for each kept item and which page gave it. If an item has several dates (adopted, published, in force, applies from), use the published or changed date for filtering and keep the others as key dates.
3. Items dated before the window are excluded. Mention at most one line of context for each, labelled "outside window".
4. If an item's date could not be established from an official page, do not guess: mark "Unconfirmed: date" and list it in the gaps.
5. Sources left with no kept items go forward as null rows (handled in `rw-render-verify`).
