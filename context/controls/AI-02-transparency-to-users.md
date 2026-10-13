# Control card AI-02: Transparency to users

**Source document:** `controls.md` ([Drive](https://drive.google.com/file/d/1FpJGay2JrDBbXLslzte0pXWH1FXkfyUH/view?usp=drivesdk)), section "AI-02".
**SAMPLE DATA.** The source says: "three constructed controls for the workshop · not FloQast's controls ... The mappings are samples; confirm with Legal." Never present this as an operating FloQast control. The product brief says how the AI Assistant discloses itself is "not stated publicly; confirm internally", so this control's description must not be used to answer that question. Fields marked (derived) are inferred, not written in the source.

- **Intent:** people know when they are talking to an AI system, and know which text an AI system drafted.
- **System it covers (derived):** the AI Assistant's first-open notice and AI Variance Analysis's in-product "AI draft" label and audit-trail field. "The control covers what users see inside the product."
- **How it works:** the AI Assistant shows an AI-system notice the first time a user opens it, reopenable from its header. Each AI Variance Analysis flux explanation carries an "AI draft" label until a preparer accepts or edits it; the audit trail records that the accepted explanation was AI-assisted. The product manager checks notice and labels in each release's acceptance test. Frequency: per release. Owner: product manager, Close Management.
- **Population it covers (derived):** AI Assistant users and AI Variance Analysis explanations inside the product. Detect is not mentioned. Exported reports are not covered.
- **Evidence it produces:** release acceptance test records with screenshots of the notice and labels; the audit-trail field specification.
- **Maps to (as written in the sample, unverified):** ISO/IEC 42001 Annex A A.8.2, A.8.5, A.9.4; EU AI Act Art. 50(1) and 50(2); Responsible AI Policy 4.3.

## Watch for

- Rules or guidance on telling users they are dealing with an AI system (EU AI Act Art. 50(1) guidelines, US state chatbot laws): the first-open notice must meet whatever form they set (once versus every session, wording, accessibility).
- Rules or guidance on marking AI-generated text (Art. 50(2), codes of practice, guidelines on the business-use carve-out): the control marks text inside the product only.
- Gap, my reading: the label is "until a preparer accepts or edits it" and the control does not cover exports. A marking rule that reaches reports sent to the CFO or auditors is outside this control's stated scope.
- Changes in exemptions for obvious-AI interaction or for human-reviewed text: either could narrow or widen what this control must do.
