# START HERE — VA Claim System (Simplified)

**Read this file once. Then resolve the tracker (Step 0 below) and keep it
open for the entire process.**

## What this system is
A linear process that discovers claims, builds source-traced evidence, and
tracks status without AI fabrication. Three files ship; the fourth — your
tracker — is generated on first run, so it is always yours and never anyone
else's data.

## The files
1. **START_HERE.md** (this file) — orientation
2. **Scout.md** — discovery, gap analysis, threshold and pattern scans
3. **Build_Evidence.md** — all generation steps in order
4. **Tracker.md** — the single living status table (protected dossier).
   Not shipped. Generated in Step 0.

## Exact process
0. **Resolve the tracker.** Ask the veteran: "Do you already have a claim
   tracker? (file path, Drive location, or 'none'.)" If one is named, Scout
   writes there — it never spawns a parallel tracker or maintains two live
   sources of truth. If none, generate Tracker.md now, in the veteran's own
   folder, from the schema at the bottom of this file. Keep the resolved
   tracker open for the entire process.
1. Open Scout.md.
2. Type one of these commands:
   - `Claim Scout, walk me through it.` (if you are unsure)
   - `Claim Scout, run everything.` (if records are ready)
3. Copy the resulting CLAIM STATE / EVIDENCE STATE / NEXT ACTION lines into the resolved tracker.
4. Look at the Next Action column in the tracker. It will point to a section inside Build_Evidence.md.
5. Open that section only. After finishing, update only the status columns in the tracker.
6. Repeat until the Next Action says Ready to File or Closed.

## Rules that never change
- No source → no fact
- No fact → no claimed evidence
- No medical source → no AI-generated medical opinion
- No human verification → no final personal statement
- Never invent symptoms, thresholds, or nexus language
- Never delete historical rows in the tracker
- Every module writes back to the tracker — nothing runs, or matters, outside the tracked state

## Where to get your data (upload checklist)
Upload as many as you have before the first Scout run:
- VA Blue Button Report (VA.gov → My HealtheVet → Blue Button → Select All)
- DD-214 for every period of service
- All VA Rating Decision Letters (including denials)
- C&P exam reports
- Service Treatment Records
- Private medical records
- Prior claim or appeal filings

You can add more records later. Every section in Build_Evidence.md will re-scan new material.

## What this system deliberately does not do
- Predict ratings or effective dates
- Coach or script what to say in a C&P exam
- Draft buddy or impact statements without a source quote
- **Definitively declare** that VA made an error — potential factual errors are flagged for human/representative review only (see Build_Evidence.md Section 5 and Scout.md's Red Team Phrase Scan), never asserted as fact
- Auto-merge anything into a single "claim package"

## What this system checks, without predicting anything
- Whether known regulatory thresholds (TDIU's 40/70 rule, SMC criteria) are met, close, or unmet by what's already documented — a threshold check against your own sourced facts, not a rating prediction
- Whether known causal/aggravation chains between diagnosed conditions exist in your record (Kinetic Chain Scan) — a pattern match against your own sourced facts, not a new diagnosis
- Whether VA-adverse language ("resolved," "stable," "not service-connected," etc.) or gaps of 2+ years without treatment appear anywhere in your uploaded records (Red Team Phrase Scan) — a search of what's already there, not a generated argument
- Whether two identified conditions might share the same underlying manifestation before being treated as separately ratable (Pyramiding / Overlap Guard) — a flag for review under 38 CFR § 4.14, not a merge decision
- Which dates in your history are candidates worth review for effective-date purposes (Effective-Date Candidates) — a list of dates to check, never an asserted or predicted effective date
- Whether an existing plan document's logged items still hold up against new records (`Claim Scout, audit my living plan`) — produces findings to copy in, never edits the plan directly

When in doubt, look at the Next Action cell in the tracker. That is the only instruction that matters.

---

## Tracker schema (Step 0 generation mold)

When no existing tracker is named, generate Tracker.md from this schema,
verbatim except for the Event Log's first entry (date it today). Do not
improvise columns, sections, or constraints.

```markdown
---
title: "Claim Tracker — Live Status"
type: dossier
purpose: "Single source of truth for claim lifecycle state. Status fields only. Portable across AIs."
role_for_ai: "Read frontmatter and constraints first. Update only the status table and human checklist. Never invent conditions, never write functional language, never delete historical rows, never resolve conflicts silently, never add model names or signatures."
constraints:
  - "Only the columns Condition | Claim State | Evidence State | Next Action | Blocking Issue | Last Updated may be written"
  - "No narrative, no F.A.C.T. language, no doctor scripts, no opinions, no medical content"
  - "Existing rows may not be deleted; mark Closed or move to Event Log"
  - "Every status change must carry [Epistemic: Certain — source] or [Epistemic: Conflict — ...]"
  - "History entries may record only the action performed and the date. Never include an AI model name, session ID, or self-identification."
  - "Owner Notes may be written only by the human owner or by an AI explicitly instructed by the owner to act as scribe. Any other AI must leave Owner Notes untouched."
  - "When this file is loaded alone, ask the user for direction before any edit"
  - "Blocking Issue may carry Kinetic Chain, TDIU/SMC threshold, Red Team phrase-scan, Pyramiding/Overlap, effective-date-candidate, or cross-decision-inconsistency flags from Scout.md/Build_Evidence.md — same column, no new columns added"
  - "AI may assign epistemic tags to new claims from a fresh analysis pass and may propose upgrades to existing tags, but may never raise an existing tag on its own — promotion requires the human owner (or a reviewer the owner designates) to verify the receipt"
  - "Concurrency: before writing, note the last_updated value loaded; before saving, re-check it. If it changed, stop and ask the owner whether to merge, re-load, or override — never silently overwrite another session's edits"
integrity:
  required_epistemic_tags: ["Certain", "Likely", "Conflict"]
  rule: "Untagged status changes are invalid"
status: active
version: "1.0"
last_updated: ""
next_action: "Awaiting first Scout run"
---

# Claim Tracker

**Purpose:** Tracks claim lifecycle state per condition. Status only. Pair with Scout.md and Build_Evidence.md. This file was generated for you on first run — your data lives here, nowhere else.

## Core Record

| Condition | Claim State | Evidence State | Next Action | Blocking Issue | Last Updated |
|-----------|-------------|----------------|-------------|----------------|--------------|

*Rows are added by Scout runs — one per condition. Read the frontmatter constraints before writing.*

## Event Log

- [<today's date>] Tracker generated on first run. Ready for first Scout run.

## Quarantine

(empty)

## Owner Notes

(empty — human only)

## Human Affirmation Checklist (complete before filing or submitting review)

- [ ] I have read the full evidence chain for this condition
- [ ] Every functional or narrative statement carries a source quote or "Not stated by veteran — do not invent"
- [ ] No field contains a detail I cannot personally confirm under oath
- [ ] I understand any "Do Not Chase" or "STOP" flag and have addressed it or accepted the risk
- [ ] I have verified any citation myself against a primary source
- [ ] I understand that any Kinetic Chain, Threshold Check, or Red Team flag is a pattern match to investigate — not a finding, diagnosis, or proof of entitlement on its own

**Veteran signature/initials:** _______________  **Date:** _______________
```
