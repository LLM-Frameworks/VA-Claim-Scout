# Build_Evidence.md — Sequential Evidence Generation

**Read the current Tracker.md row for the condition before every section.**
**Update only the status columns in Tracker.md after every section.**
**If new records have been added since the last update, re-scan them first.**

Never invent symptoms, thresholds, compensatory behaviors, or nexus language.
Every functional claim must carry a source quote or the exact marker "Not stated by veteran — do not invent."

---

## Section 1 — PCP Secure Message (Medical Development)

**When Tracker Next Action points here.**

### Purpose
Draft a short, neutral VA Secure Message that elicits objective clinical language without appearing to solicit disability documentation.

### Rules
- Absolute neutrality. Never use "service-connected," "for my rating," "secondary to," "nexus," or "disability."
- Default ≤ 150 words.
- Use only timelines, medications, and symptoms the veteran has supplied.
- End every draft with: "Save this sent message and the provider's reply as a PDF for your claim file."

### Clinical Relationship Question (use this form)
"Doctor, could you explain whether you believe there is a medical relationship between my [condition/medication] and [other condition/symptom]? If so, what is the medical reasoning for your opinion, including whether it causes, contributes to, or aggravates the other condition?"

### Output
- Target Provider
- Subject line
- Message text
- Clinical Strategy Note (what chart language is sought)
- SOURCE TYPE IF ANSWERED: Provider documentation

### Tracker Handoff
Update Evidence State and Next Action.
After the reply is archived, move to Section 2 (FACT).

---

## Section 2 — F.A.C.T. Extractor (Evidence Extraction)

**When Tracker Next Action points here or a new source (provider reply, statement, record) is ready.**

### Purpose
Convert any documented source into objective, source-traced functional findings. Zero fabrication.

### Three-State Rule
- SUPPORTED — explicitly documented, with quote
- NOT STATED — do not invent (use this exact phrase for veteran statements)
- NOT APPLICABLE

**Finding vs. Attribution Check (apply before scoring Interpretation Confidence):** If this entry links a documented diagnosis to a *different* symptom or condition (e.g., "arthritis is causing my insomnia," "the back condition is why my hip hurts"), tag the diagnosis itself SUPPORTED but tag the causal link separately as NOT STATED / provider-unconfirmed unless a provider reply or medical opinion explicitly makes that connection. Do not let a Tier 1 diagnosis (see Scout.md Section 2) raise the confidence of an unconfirmed causal claim riding on it.

### Required Fields (every entry)
- Source Type (Veteran report | Provider documentation | Diagnostic test | C&P examination | Service record | Lay/buddy | VA decision | Other)
- Condition
- Original Content (exact quote)
- Stoic Language Flagged
- Interpretation Confidence (1–5). ≥4 auto-flags for review
- Contradiction Check
- F.A.C.T. breakdown with source quotes:
  - Functional Trigger
  - Acute Symptom
  - Compensatory Behavior
  - Downstream Impact
  - Functional Cost (what completing the task cost, if described)
- Evidence Quality Score (seven dimensions: Source Quality, Objectivity, Specificity, Temporal Proximity, Medical Support, Functional Detail, Contradiction Risk)
- CP Exam Talking Point (observation first, reported consequence second)
- VA Form 21-4138 block (same rule)
- Probe questions for any missing quantifiable thresholds

**Disclaimer (mandatory):** Do not submit this language if the veteran cannot personally confirm every detail under oath.

### Tracker Handoff
Save the full entry as a dated artifact.
Update Evidence State in Tracker.md.
Confidence ≥4 or any unresolved contradiction → flag in Quarantine.

---

## Section 3 — C&P Exam Prep

**When Tracker Claim State = C&P/EXAM or Next Action points here.**

### Purpose
Prepare the veteran to accurately explain what the record already establishes. Never coach what to say.

### Firewall
- Never tell the veteran what number, word, or symptom to report
- Never generate a rehearsed script
- Never invent a threshold the veteran has not stated

### Required Sections
1. Exam Purpose (from actual request/DBQ, not assumed)
2. Know Your Record (Documented Facts vs Things the Record Does Not Establish)
3. Symptom Timeline (dates + sources only)
4. Functional Cost Framing — "Do not equate task completion with absence of impairment." Prompt structure only; never fill answers.
5. Frequency / Duration / Severity Gaps — list what is Established vs Not established; generate questions, never numbers.
6. Mandatory warning (verbatim): "This is preparation, not a script. Do not memorize or recite… If you don't know, say you don't know."
7. Examiner Question Bank (blanks for veteran's own answers)
8. Contradiction Review (present, do not resolve)
9. Favorable / Unfavorable / Ambiguous Evidence (list all three honestly)
10. Red Flag Detector (preparation only)
11. Exam Day Mode (10 short rules)
12. Post-Exam Recall Capture (immediate, labeled "Veteran's contemporaneous recollection — not yet verified")

### Tracker Handoff
Set Claim State = C&P/EXAM.
After exam, update Next Action to "Awaiting C&P report" or "Run Section 4."

---

## Section 4 — C&P Exam Analyzer

**When the official C&P report arrives.**

### Purpose
Post-exam audit only. Compare report vs veteran recall vs existing record. Flag potential issues for human review. Never assert examiner error.

### Audit Checklist
A–L items (correct condition, diagnosis supported, history accurate, objective findings, functional impairment, flare-ups, testing, medical opinion, rationale, internal contradictions, contradictions with record, omitted evidence).
Every "NO" or "UNCLEAR" gets exactly: "Potential issue for human review: [specific gap]."

### Recall vs Report
Veteran recalled: "…"
Report states: "…"
Match / Partial / Discrepancy — not yet explained. Do not decide which is correct.

### Tracker Handoff
Update Claim State to RATING.
Log any Blocking Issue.
Add C&P report to evidence (Source = C&P examiner, Provenance = VA).

---

## Section 5 — Decision Decoder & Review Router

**When a VA decision letter arrives.**

### Purpose
Extract what the decision actually says, compare stated reasons against the record, and list possible review pathways. Never assert VA made an error — flag potential factual error for human/representative review only.

### Extraction
ISSUE / DECISION / RATING / EFFECTIVE DATE / FAVORABLE FINDINGS / UNFAVORABLE FINDINGS / EVIDENCE RELIED UPON / REASONS FOR DECISION (verbatim quotes).

### Mandatory Check
Denial Reason vs. Record Check — for every stated reason: Match or CONTRADICTED. Flag potential factual error separately from missing-evidence gaps. A CONTRADICTED flag is a signal for human/representative review, not a conclusion that VA erred.

### Cross-Decision Check
If two or more decisions exist for the same veteran (e.g., a rating reduction and a later grant/denial), compare the stated reasoning of each against the other — not just each decision against the record in isolation. Flag any case where one VA decision's stated rationale is in tension with another VA decision's stated rationale for a related condition (example: a reduction premised on "improvement" versus a later decision describing ongoing severity from the same condition). Output:
```
DECISION A:  <date, issue, stated reasoning quote>
DECISION B:  <date, issue, stated reasoning quote>
TENSION:     <one-line description of the apparent conflict>
STATUS:      POTENTIAL CROSS-DECISION INCONSISTENCY — for human/representative review
```
This is a flag, not an assertion that either decision was wrong.

### Gap Analysis
MISSING/UNADDRESSED EVIDENCE
POTENTIAL FACTUAL ERROR
POTENTIAL CROSS-DECISION INCONSISTENCY
POTENTIAL MEDICAL OPINION PROBLEM
POTENTIAL DEVELOPMENT ISSUE

### Review Router (possible paths only)
- New evidence VA didn't have → Supplemental Claim may fit
- Existing evidence appears misread → Higher-Level Review may fit
- Legal/procedural/complex → Board Appeal may fit
Always state why the other paths were not selected. Verify eligibility, evidence rules, and deadlines with a VSO or accredited attorney.

### Tracker Handoff
Update Decision State and Claim State (REVIEW REQUIRED / GRANTED / DENIED / etc.).
Log Blocking Issues if Supplemental Claim is contemplated, including any POTENTIAL CROSS-DECISION INCONSISTENCY flag.

---

## Section 6 — Timeline (Case-Wide)

**Run after major evidence additions or before filing.**

### Purpose
One master chronology across all conditions. Detect gaps and date patterns. Never interpret legal significance.

### Output
DATE | EVENT | SOURCE | CONDITION(S) | EVIDENCE CREATED | VA ACTION | NEXT DEADLINE

### Pattern Flags (observation only)
GAP / UNEXPLAINED DELAY / DIAGNOSIS-BEFORE-FILING / TREATMENT-BEFORE-DIAGNOSIS / CLAIM-BEFORE-DIAGNOSIS / SEVERITY CHANGE / CONFLICTING DATES / CONTINUOUS PURSUIT QUESTION

Each flag includes a one-line "why this might matter" note and is left unresolved for human/representative review.

### Tracker Handoff
Save chronology as dated artifact.
Update any Blocking Issue created by a pattern flag.

---

## Section 7 — Buddy & Impact Statement Generator

**When Tracker Next Action points here, or on explicit request.**

### Purpose
Draft a starting-point buddy or impact statement built only from source quotes and veteran-supplied detail already logged in Section 2 (FACT). Never generate generic or templated language, and never invent an observation, symptom, or example the veteran or witness has not personally supplied.

### Firewall
- Every sentence must trace to a FACT entry, a veteran-supplied detail, or the exact marker "Not stated — do not invent."
- Never draft on a condition with no Section 2 entry yet — route back to Section 2 first.
- Never write a medical opinion into a buddy statement; buddy statements describe what was observed, not what was diagnosed.

### Buddy Statement — Required Structure (VA Form 21-10210 format)
1. Who I Am / relationship to the veteran
2. How I know the veteran (duration, context)
3. What I have personally observed (source-traced only)
4. Specific examples (dates/approximate timeframes, from FACT entries or direct witness input)
5. How it affects the veteran (functional impact, source-traced only)
6. Closing affirmation, signature block, relationship, date

### Impact Statement — Required Structure
Four domains, each source-traced only, worst-day framing: Work Life, Social Life, Family Life, Sexual/Intimate Functioning (use clinical, matter-of-fact language; do not omit this domain solely because it is sensitive).

### Mandatory Notice (include with every draft)
"This is a starting point, not a finished document. Review it, correct anything that does not match your actual experience, rewrite it in your own words, and sign only what you know to be true under oath."

### Tracker Handoff
Update Evidence State to note a drafted-but-unverified buddy/impact statement exists for the condition.
Do not change Claim State until the veteran confirms the statement is finalized and signed — at that point, log it as a new Source Type: Lay/buddy entry per Section 2's rules.

---

## Section 8 — Case Summary

**Run on request, or when Tracker shows Ready to File for any condition.**

### Purpose
Compile what already exists across Tracker.md and prior sections into a single reference document for the veteran, VSO, or attorney. Generates no new facts, opinions, or predictions — this is reformatting only.

### Required Structure
1. **Conditions Overview** — pulled directly from Tracker's Core Record: Condition | Claim State | Evidence State | Next Action | Blocking Issue
2. **Evidence Gaps** — pulled directly from each condition's Missing Link Engine output (Scout.md Section 4)
3. **Open Flags** — any CONTRADICTED, POTENTIAL FACTUAL ERROR, or POTENTIAL CROSS-DECISION INCONSISTENCY flags from Section 5, and any unresolved Red Team Phrase Scan entries from Scout.md Section 11
4. **Chains and Thresholds Identified** — any Kinetic Chain Scan or TDIU/SMC Threshold Check results from Scout.md Sections 9–10, labeled PATTERN MATCH ONLY / MET / CLOSE / NOT MET as originally output
5. **Supporting Documents** — clean list of records that informed the analysis, with type/date/source only

### Mandatory Notice
"This summary compiles existing tracked status only. It does not predict a rating, assert that VA made an error, or constitute legal or medical advice. Review with a VSO, accredited claims agent, or VA-accredited attorney before taking action."

### Tracker Handoff
Log the generation date as an Event Log entry in Tracker.md: "[date] Case Summary generated." No status column changes.

---

## Final Rule
After every section, return to Tracker.md and update only the status columns.
The Next Action cell is the only instruction the next AI or the user needs.
