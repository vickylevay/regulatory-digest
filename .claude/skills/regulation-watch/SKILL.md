---
name: regulation-watch
description: Run the full regulation watch for FloQast's AI features. Use when asked to run the regulation watch, produce the regulatory digest, or report which AI regulations or guidance published since a date apply to AI Assistant, AI Variance Analysis and Detect.
---

# Regulation watch (entry point)

Read `CLAUDE.md` (parameters, product facts, rules) first. Context and sources are read in step 2, before anything is written.

1. **Fix the window and date.** Record `window_start` (default 2026-07-01 if none given) and `window_end` (today's date from the environment). Do not assume the date.
2. Invoke `rw-load-context`: read `context/index.md`, the product card and `sources.md`; build the watch list.
3. Invoke `rw-gather`: fetch each allowed source, steered by the watch list; record page URLs and page dates.
4. Invoke `rw-filter-window`: keep only items dated inside the window.
5. Invoke `rw-load-context` again for the control cards the index matches to each kept item, then `rw-assess`: map each item to features and rate impact.
6. Invoke `rw-render-verify`: add null rows, render the table, gaps and three actions, then run the verification checklist before sending.

Do not write any part of the answer until step 2 is done.

Same window and same source state must give the same structure, row order, ratings and gap list.
