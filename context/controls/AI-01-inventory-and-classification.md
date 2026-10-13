# Control card AI-01: AI system inventory and classification

**Source document:** `controls.md` ([Drive](https://drive.google.com/file/d/1FpJGay2JrDBbXLslzte0pXWH1FXkfyUH/view?usp=drivesdk)), section "AI-01".
**SAMPLE DATA.** The source says: "three constructed controls for the workshop · not FloQast's controls ... The mappings are samples; confirm with Legal." Never present this as an operating FloQast control. Fields marked (derived) are inferred from the description, not written in the source.

- **Intent:** every AI feature is known, classified and assessed before it reaches a customer, and again when it changes.
- **System it covers (derived):** the AI system inventory kept by the AI governance lead. It records what a feature does inside the product (purpose, model, data read, outputs produced). It "does not record the paths by which outputs leave it."
- **How it works:** before release the product manager registers the feature, classifies it under the EU AI Act risk tiers, checks it against US state rules on automated decisions and completes the impact assessment; the AI governance lead approves. Entry and assessment are updated at each material change. Frequency: at release and each material change; inventory reviewed quarterly. Owner: AI governance lead.
- **Population it covers (derived):** every AI feature before release and at each material change. The source does not list the features.
- **Evidence it produces:** the inventory with approvals and dates; the impact assessments; the quarterly review sign-off.
- **Maps to (as written in the sample, unverified):** ISO/IEC 42001 Annex A A.4.2, A.5.2, A.5.3, A.6.2.2; EU AI Act Art. 6 and Annex III; Responsible AI Policy 4.1, 4.2.

## Watch for

- Changes to EU AI Act risk-tier definitions, Annex III or classification guidance: this control's classification step depends on them.
- Changes to US state definitions of automated decision-making or consequential decision (Colorado, CalPrivacy): the control's state-rule check depends on them.
- New impact-assessment or risk-assessment duties (for example CalPrivacy risk assessments), which the impact-assessment step may need to absorb.
- Changes to ISO 42001 or NIST AI RMF material that alter what an inventory should record.
- Gap, my reading: the inventory does not record output paths, so a rule about where AI output ends up (for example exported reports) is not caught by this control.
