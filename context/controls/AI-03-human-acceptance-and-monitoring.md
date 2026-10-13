# Control card AI-03: Human acceptance and monitoring of AI outputs

**Source document:** `controls.md` ([Drive](https://drive.google.com/file/d/1FpJGay2JrDBbXLslzte0pXWH1FXkfyUH/view?usp=drivesdk)), section "AI-03".
**SAMPLE DATA.** The source says: "three constructed controls for the workshop · not FloQast's controls ... The mappings are samples; confirm with Legal." Never present this as an operating FloQast control. The product brief says log retention and AI incident reporting are "not stated publicly; confirm internally", so this control's twelve-month figure must not be used to answer that. Fields marked (derived) are inferred, not written in the source.

- **Intent:** no AI output changes a customer's financial records without a person, and the features are watched for drift.
- **System it covers (derived):** the acceptance step in the product (AI Variance Analysis explanations, AI-drafted comments), Detect flags, and the event logs and monthly monitoring review for the AI features.
- **How it works:** the product will not save an AI-drafted explanation or post an AI-drafted comment until a named user accepts it; a Detect flag never changes a balance or a sign-off. Monthly, the engineering manager reviews acceptance and edit rates and reported errors per feature against agreed thresholds and opens a ticket when one is crossed. Event logs (prompt, output, user, time, acceptance) are kept for twelve months. Customer-affecting incidents go through the incident procedure. Frequency: continuous (acceptance); monthly (monitoring review). Owner: engineering manager, Close Management.
- **Population it covers (derived):** AI-drafted explanations, AI-drafted comments, Detect flags. The AI Assistant's journal-entry fixes are not named; the brief says they are applied after the user approves them, so whether this control covers them needs confirming (my observation).
- **Evidence it produces:** the acceptance-step design and its test; the monthly monitoring review; the log retention configuration; incident tickets.
- **Maps to (as written in the sample, unverified):** ISO/IEC 42001 Annex A A.6.2.6, A.6.2.8, A.8.4, A.9.2; EU AI Act Art. 14, 72 and 73 (where high-risk); Responsible AI Policy 4.4, 4.5.

## Watch for

- Changes to the high-risk definition or to when Art. 14, 72 and 73 apply: the mapping is conditional ("where high-risk") and currently rests on the features not being high-risk.
- Record-keeping, log-retention or incident-reporting rules, in the EU or elsewhere: the control keeps logs for twelve months and relies on the general incident procedure.
- Human-oversight guidance that defines what meaningful review means: a rule that sets a standard for the acceptance step.
- NIST or ISO material on monitoring, drift and performance measurement: the monthly review thresholds.
- Any new AI feature that acts without per-item acceptance (agents, automatic posting): outside the control's stated population.
