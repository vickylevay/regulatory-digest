# Context index

Read this first. It says what context exists, when to open each card, and how far to trust it. Cards are internal context about FloQast's product and controls. They are not regulatory sources.

## Cards

| Card | Covers | Open when |
|---|---|---|
| [product/close-management-ai-features.md](product/close-management-ai-features.md) | AI Assistant, AI Variance Analysis, Detect: what each does, users, data, where output goes, rules and audits that touch them, confirm items, watch for | Always, on every run |
| [controls/AI-01-inventory-and-classification.md](controls/AI-01-inventory-and-classification.md) | Inventory, risk-tier classification, impact assessment | Item is about risk classification, high-risk or Annex III scope, definitions of automated decisions or consequential decisions, risk or impact assessments |
| [controls/AI-02-transparency-to-users.md](controls/AI-02-transparency-to-users.md) | AI-system notice in the Assistant, "AI draft" labels in Variance Analysis | Item is about disclosure to users, chatbots, marking or labelling AI-generated content, Art. 50 guidelines or codes of practice |
| [controls/AI-03-human-acceptance-and-monitoring.md](controls/AI-03-human-acceptance-and-monitoring.md) | Human acceptance step, Detect flags, monitoring, logs, incidents | Item is about human oversight, logging and record-keeping, monitoring, incident reporting, post-market obligations |

If an item fits none of these, still read the product card, and say in the row that no control card matched.

## How far to trust the cards

- **Product card:** built from public floqast.com pages opened 12 October 2026. Lines marked **confirm** are unknown, not "no". Treat them as open questions.
- **Control cards:** SAMPLE DATA constructed for a workshop, "not FloQast's controls". The mappings are samples, to be confirmed with Legal. Refer to them as "sample control AI-0x". Never say FloQast operates, passes or fails one.
- **The brief's statements about what a law requires** (Art. 50(1), Art. 50(2) and similar) are its author's reading. Verify against an official page from `sources.md` before using one.

## Known gaps and open questions

Carry an entry into the digest's gaps list whenever an item depends on it.

1. Export marking: whether AI-drafted flux explanations keep a label when exported, and whether exports go to external auditors. Sample AI-02 covers only what users see inside the product.
2. AI Assistant disclosure: how and how often it tells users it is AI. Not stated publicly. Do not infer it from sample AI-02.
3. Model provider, where models run, training on customer data. Not stated publicly.
4. Log retention for AI features and AI incident reporting. Not stated publicly. Do not infer it from sample AI-03.
5. Whether a Detect flag can be attributed to a named individual (my addition). The "no decisions about individuals" fact depends on it.
6. Scope of the routine: the product brief also lists AI Agents, AI Matching, Automated Reconciliations, Journal Entry Management (posts to the ERP), AI Governance, Request Agent and Close Analytics. `CLAUDE.md` names three features. Until the owner confirms, report on the three and list the others in the gaps when an item could touch them.
7. SOC 1/2 reports and ISO 27001/27701 certificates: which exist is not stated publicly.

## Maintenance

- The two source files are in the Drive folder `1Od1TD01vYIfg75NSL1bMasdkfhfW6oAZ` (`close-management-ai-features.md`, `controls.md`). When either changes, regenerate the matching cards and update the date in the card header.
- When real FloQast controls replace the sample ones, replace the control cards and remove the SAMPLE DATA warnings and the "sample control" wording above in one change.
