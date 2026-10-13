# Regulation Watch

Instructions for the regulation-watch routine. The routine reports which AI regulations and official guidance, published or changed inside a date window, apply to FloQast's AI features. Accuracy over coverage: anything not sourced from an official page is flagged, never guessed.

Related files:
- `sources.md`: the allowed sources, their URLs and the minimum fetches per source.
- `context/index.md`: index of the product and control cards. Read it before anything else.
- `context/product/` and `context/controls/`: the cards the agent reads before writing.
- `.claude/skills/regulation-watch/`: entry point that runs the steps in order.
- `.claude/skills/rw-load-context/`, `rw-gather/`, `rw-filter-window/`, `rw-assess/`, `rw-render-verify/`: one skill per step.

## Parameters

- `window_start` (required). Default for this routine: 2026-07-01. If a run is started without one and no default applies, ask once.
- `window_end` (default: today's date from the environment; never assume the date).
- `owners` (optional): name or team per row. Not yet defined. If not supplied, print "Owner: TBC" in the table and list "assign owners" among the gaps. Never invent owners.

## Product facts (treat as given, do not re-ask)

FloQast sells Close Management, month-end close software for accounting teams, to customers in the US, UK and EU. AI features:

1. **AI Assistant**: answers users' questions about their own close (conversational, direct two-way exchange with users).
2. **AI Variance Analysis**: drafts flux explanations that accountants review; they go into reports exported to the CFO (generative text, human review, B2B).
3. **Detect**: flags unusual transactions for review.

None of them makes decisions about individuals. If the user states a change to these facts, use theirs for that run.

## Context before writing

Before gathering, read `context/index.md`, the product card and `sources.md`. Before assessing each item, read the control cards the index says match it. The `rw-load-context` skill does this. Rules:

- Cards are internal context, not regulatory sources. Regulatory claims still need an official page fetched in this run.
- The control cards are SAMPLE DATA, not FloQast's controls. Call them "sample control AI-0x" and never say FloQast operates, passes or fails one.
- Lines marked **confirm** in a card are unknown, not "no". If an item depends on one, list it in the gaps as "Unconfirmed: ...".
- If a card conflicts with the product facts above, use the product facts and list the conflict in the gaps.
- Name the card behind a feature or control judgment in the row (for example "product card", "sample control AI-02").

## Rules that never bend

- Official sources only (see `sources.md`). Never cite law-firm blogs, news, vendors or secondary summaries. Results from other sites may be used only to find the official URL.
- Every row needs a page link and a date. Every claim must trace to a page actually fetched in this run.
- Unsourced or unread means flagged: write "Unconfirmed:" plus what, and add it to the gaps list.
- Never fabricate dates, article numbers, fines, owners or quotes. Quote no more than a short phrase and attribute it.
- Legal conclusions are framed as "my reading", not legal advice. Recommend counsel for scope questions. Do not state "would" or "likely" as fact.
- If a page is blocked or fails to load, say so. Do not work around it with curl, bash fetches or archive sites.
- UK material is not covered by the allowed sources: always list UK as a gap.
- Idempotence: the same window and same source state must give the same table structure, row order, ratings and gap list. Do not add or remove rows on a re-run unless a source page changed; if one did, say which page and its new date.
- Do not create pull requests, post to Slack or send anything externally unless asked. The deliverable is the answer in the session.

## Workflow

Run the steps in order (the `regulation-watch` skill does this):

1. Fix the window and date.
2. Load context: index, product card, sources note (`rw-load-context`).
3. Gather per source (`rw-gather`).
4. Filter to the window (`rw-filter-window`).
5. Read matching control cards, apply to features and rate impact (`rw-load-context`, then `rw-assess`).
6. Check for nulls, render and verify (`rw-render-verify`).

## Output

One table, then the gaps list, then exactly three numbered "do these first" lines. The exact format is in `rw-render-verify`. Concise, no emojis.
