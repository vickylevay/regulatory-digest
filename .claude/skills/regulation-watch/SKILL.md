---
name: regulation-watch
description: Run the full regulation watch for FloQast's AI features. Use when asked to run the regulation watch, produce the regulatory digest, or report which AI regulations or guidance published since a date apply to AI Assistant, AI Variance Analysis and Detect.
---

# Regulation watch (entry point)

Read `CLAUDE.md` (parameters, product facts, rules) and `sources.md` first.

1. **Fix the window and date.** Record `window_start` (default 2026-07-01 if none given) and `window_end` (today's date from the environment). Do not assume the date.
2. Invoke `rw-gather`: fetch each allowed source, record page URLs and page dates.
3. Invoke `rw-filter-window`: keep only items dated inside the window.
4. Invoke `rw-assess`: map each item to features and rate impact.
5. Invoke `rw-render-verify`: add null rows, render the table, gaps and three actions, then run the verification checklist before sending.

Same window and same source state must give the same structure, row order, ratings and gap list.
