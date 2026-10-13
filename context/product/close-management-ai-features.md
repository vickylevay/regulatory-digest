# Product card: Close Management AI features

**Source:** `close-management-ai-features.md` ([Drive](https://drive.google.com/file/d/1ewIBEkRYJftkceu8rH3byyo09ZHAr-WF/view?usp=drivesdk)), cited below as "Brief". The Brief is built only from public floqast.com pages opened 12 October 2026 and names the page behind each statement. It contains no internal documents.
**Status:** public information. Anything the public pages do not say is marked **confirm** and must not be treated as fact.
**Not a regulatory source.** Statements in the Brief about what a law requires are its author's reading and are not verified. Regulatory claims in a digest still need an official page from `sources.md`.

Citation form: `[Brief: section]`.

## AI Assistant

- **What it does:** answers questions about close status (open reconciliations, outstanding items, balance changes against the prior month); runs a pre-review check that flags duplicate postings, missing reversal dates, empty subledger lines and unfamiliar account and dimension pairs, scores audit risk and explains its findings; on journal entries, "approve the fixes you agree with, and it makes them". It shows its reasoning and guardrails keep it on accounting work. [Brief: Three features, 2]
- **Who uses it:** accounting teams (CFO/CAO, Controller, Accountant, Internal Audit, Compliance/Risk Manager, Finance Transformation). [Brief: Who uses them]
- **Data it uses:** the user's own close records; "existing permissions and entity access govern every answer". [Brief: Three features, 2; What Close Management is]
- **Where output goes:** shown to the user in the product; journal-entry fixes are applied only after the user approves them. [Brief: Three features, 2] Whether answers can be exported: **confirm**.
- **Rules and audits that touch it:** direct interaction with users, so the Brief points to AI-disclosure rules (EU AI Act Art. 50(1), state chatbot laws; the Brief's reading, unverified). [Brief: Why it matters] Inside FloQast's ISO 42001 audit program. [Brief: Trust and security] Sample controls AI-01, AI-02, AI-03 (see index).
- **Confirm:** how it tells a user it is an AI system, and whether once or every session; model provider, where models run, training on customer data. [Brief: Not stated publicly]

## AI Variance Analysis

- **What it does:** scans transaction data for significant swings, flags material changes and variance drivers, and drafts flux explanations for preparers; reviewers review explanations, leave notes and see what is outstanding; the system logs evidence of every sign-off. [Brief: Three features, 1]
- **Who uses it:** preparers draft and reviewers review; the CFO receives the exported reports. [Brief: Three features, 1]
- **Data it uses:** transaction data, completed reconciliations and confirmed balances, prior-period variances, budget amounts, customer-set materiality thresholds. [Brief: Three features, 1]
- **Where output goes:** flux and budget variance reports are "exported to share with the CFO" and support "board-ready reporting". [Brief: Three features, 1] Whether exports carry a label or machine-readable mark that the text was AI-drafted: **confirm**. Whether exports go to external auditors: **confirm**.
- **Rules and audits that touch it:** generates text that leaves the product in reports, so the Brief points to AI-generated-content marking (Art. 50(2) and its guidelines, including the business-use carve-out condition "not intended for sharing outside the organisation"; the Brief's reading, unverified). [Brief: Why it matters] ISO 42001 audit program. Sample controls AI-01, AI-02, AI-03.
- **Confirm:** export labelling and auditor sharing (above); log retention. [Brief: Not stated publicly]

## Detect

- **What it does:** monitors the general ledger continuously with AI and custom rules to catch anomalous transactions; logs every review and sign-off. A flag is a prompt to review; the page describes no automatic change to a balance. [Brief: Three features, 3]
- **Who uses it:** the same accounting-team roles. [Brief: Who uses them]
- **Data it uses:** the general ledger, synced from the customer's ERP (NetSuite, SAP, Workday, Microsoft, Sage Intacct, Xero named on the site). [Brief: Three features, 3; Integrations] Whether ERP data is the only input: **confirm**.
- **Where output goes:** flags to a reviewer inside the product. [Brief: Three features, 3] How flags are explained to the reviewer: **confirm**.
- **Rules and audits that touch it:** none named in the Brief beyond the ISO 42001 audit program. Sample controls AI-01, AI-03.
- **Confirm (my addition, not in the Brief):** whether a flag can be attributed to a named individual such as an employee. The "no decisions about individuals" fact depends on this.

## Across the product

- **Markets and users:** customers in the US, UK and EU (routine product facts in `CLAUDE.md`); the Brief says "3,500+ global companies". [Brief: Who uses them]
- **Also in the Close AI line, not in the three-feature list the routine watches:** AI Agents (an accountant signs off before an agent runs), AI Matching, Automated Reconciliations, Journal Entry Management (creates and posts journals to the ERP), AI Governance (COSO-aligned), plus Request Agent and Close Analytics with no description. [Brief: The Close AI line] Whether the routine should cover them: **confirm** (see index).
- **Published trust position:** SOC 3 public; SOC reports to customer admins; "a pioneer and early adopter of ISO 42001"; agents "audited against the COSO GenAI Framework"; Data Privacy Framework notice. [Brief: Trust and security] Which SOC 1/2 reports and ISO 27001/27701 certificates exist: **confirm**.

## Watch for

Changes that land inside this product's boundary:

- Disclosure duties when users interact with an AI system (EU, US state chatbot laws): AI Assistant.
- Marking or labelling duties for AI-generated text, and guidance on what "shared outside the organisation" means: AI Variance Analysis exports to the CFO and possibly auditors.
- Definitions that decide whether decisions about individuals are involved (consumer, consequential decision, automated decision-making): re-checks the "no decisions about individuals" fact for all three features.
- Changes to high-risk classification, Annex III, or the timing of high-risk obligations: currently Low on the stated facts, but rises if any feature touches individuals.
- Duties for model providers and downstream deployers, and rules on training with customer data: model provider is not stated publicly.
- Logging, record-keeping and incident-reporting rules: log retention and incident reporting are not stated publicly.
- AI governance standards and frameworks FloQast claims alignment with: ISO 42001, COSO GenAI, NIST AI RMF.
- Features that act rather than advise: AI Assistant journal-entry fixes, AI Agents, automatic posting to the ERP.
