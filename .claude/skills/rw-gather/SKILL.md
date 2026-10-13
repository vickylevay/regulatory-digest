---
name: rw-gather
description: Step 2 of regulation watch. Fetch each allowed official source (EC AI Act pages, EUR-Lex, Colorado AG, CalPrivacy, NIST) and record items with URL and dates. Use when gathering regulatory material for the window.
---

# Gather

Inputs: `window_start`, `window_end`, `sources.md`, and the watch list from `rw-load-context`.

1. Load WebSearch and WebFetch via ToolSearch if not already loaded.
2. For each of the five sources in `sources.md`, run in parallel where possible:
   a. WebSearch restricted with `allowed_domains` to that source's domains.
   b. WebFetch the primary page directly and the minimum fetches listed in `sources.md`.
   c. Read the page's own published, modified or last-updated date.
3. Use the watch list to pick search terms and to decide which linked items to open in full. Still open every minimum fetch in `sources.md`, and do not drop an in-window item because it matches nothing on the watch list: record it, and let `rw-assess` rate it Low.
4. For large PDFs, save to the scratchpad and Grep for key definitions instead of reading everything. Keep a note of what was read in full, what was only grepped, and what was not opened.
5. If a page fails or is blocked, record the failure. Do not use curl, bash fetches or archive sites.
6. Output a raw list per source: item title, URL, date found, which page gave the date, what was read of it. Include sources with no items, with the page and date checked.

Do not use search-result snippets from non-official sites as evidence.
