# Claim Scout — Requirements

**Version:** 0.4 — DRAFT
**Date:** 2026-09-27
**Status:** Proposed. Not in force until owner approves.
**Owner:** Bill Barrett

Further requirements to be added. Each new requirement gets an ID, plain wording, and a test.

---

## R1 — Simple to use (headline requirement)

A veteran with no prior knowledge of the system can upload records and get a useful first output in a single session, guided only by the tool itself. No manual, no tutorial, no prior reading.

- **Test:** hand the system to someone who has never seen it. If they stall, the system failed — not the user.

## R2 — Guided first, power on demand

The guided intake (`walk me through it`) is the default path. Power commands exist for experienced users but are never required to get value.

- **Test:** every capability reachable by a power command is also reachable through the guided path.

## R3 — Plain language, always

No VA jargon, legal term, or acronym appears in output without a plain-English definition on first use in that output.

- **Test:** a non-veteran reader understands every output without looking anything up.

## R4 — No dead ends

Every output states three things: what was found, the single most useful next step, and what is missing. The user never has to ask "okay, so what now?"

## R5 — Missing records are named, never skipped

If records are absent, the output says which ones and why they matter — then proceeds with what exists. Silence about gaps is a defect.

## R6 — Tracker stays portable

Tracker.md remains a standalone, human-readable file that any person or any AI can use without the rest of the system. No feature may make the Tracker depend on tooling outside the file.

## R7 — Command economy

New capabilities must not add new commands unless they remove real ambiguity. Prefer fewer, clearer commands over more features. If two commands confuse users, merge them.

## R8 — Simplicity never overrides the firewall

Simple to use, never simple-minded. No-source-no-fact, the evidence tiers, the Finding vs. Attribution rule, and the Citation Confidence rule hold regardless of how simple the interface gets. If a simplification would weaken a guardrail, the simplification loses.

## R9 — Uncertainty is stated, not buried

Low confidence, conflicts, and unknowns appear in the output in plain words, at the point where they matter — not in a footnote, not omitted for cleanliness.

## R10 — Tracker governance takes effect only on owner approval

The Tracker rules file, Review Protocol/Log, and signed-entry convention are inert until the owner explicitly approves the draft. Approval triggers the queued application steps in order: concurrency recheck, upload as Tracker-Rules.md v1.0, pin `rules_version` in Tracker-2, add the Review Log, apply signed entries going forward. No partial application — the governance package goes live whole or not at all.

- **Test:** inspect the live Tracker. Any governance element active without a recorded owner approval means the gate failed.

## R11 — Recruit on pain, not politeness

User testing recruits veterans who already feel the problem — not friends doing a favor. A direct ask produces polite yeses with no desire behind them: the 2026-09-22 Claim Scout pilot drew zero real testers this way, even free. A tester must want the help before being asked.

- **Test:** ask each tester what they were already doing about the problem before you contacted them. If the answer is "nothing," they don't count.

## R12 — One tracker, not two

Claim Scout asks for the veteran's existing claim tracker at the start of a run and writes there. It never spawns a parallel tracker or maintains two live sources of truth. When no existing tracker is named, Tracker.md is generated on first run from the schema in START_HERE.md — it is never shipped, bundled, or reused.

- **Test:** run Scout twice, naming an existing tracker both times. If a second live tracker file gains rows, the system failed.

## R13 — VA decisions are opinions, not facts

A VA rating decision — including its denial rationale and any examiner opinion it rests on — is treated as an assertion to be tested, never as a finding of fact. Scout separates what a decision concedes or documents (fact) from what it concludes or interprets (opinion), and red-teams the opinions.

- **Test:** feed Scout a denial letter. If any output states the denial's rationale as fact without an opinion tag and a red-team pass, the system failed.

---

## Change log

- 2026-09-29 — R12 refined in draft: tracker is generated on first run from the START_HERE.md schema, never shipped/bundled/reused (owner's "ship the mold, not the casting" call). START_HERE.md gained Step 0 (tracker resolution) and the embedded schema; Scout.md's three "bundled Tracker.md" references updated. Still DRAFT, awaiting owner review.
- 2026-09-27 — v0.4: added R12 (one tracker — ask for the existing tracker, never spawn a parallel one) and R13 (VA decisions are opinions, not facts — red-team the denial). Still DRAFT, awaiting owner review.
- 2026-09-22 — v0.3: added R11 (recruit on pain, not politeness — testers must want the help before being asked; lesson from the pilot that drew zero real testers). Still DRAFT, awaiting owner review.
- 2026-09-22 — v0.2: added R10 (tracker governance approval gate). Still DRAFT, awaiting owner review.
- 2026-09-22 — v0.1 drafted (Muse / Muse Spark). Nine requirements. Awaiting owner review.
