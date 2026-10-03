# Claim Scout

**A plugin in the [LLM Frameworks](https://github.com/LLM-Frameworks) library — a free AI framework that helps veterans navigate VA disability claims.**

Claim Scout gives you the analytical perspective of a VA-accredited attorney, a claims rater, and a VSO — without the cost. Load it into any capable AI and ask it to help you understand your records and your claim.

It is one plugin in the LLM Frameworks library: a collection of logic frameworks for evaluating claims of any kind. The same machinery runs underneath all of them — evidence tiers, source receipts, and a hard rule against fabrication.

---

## What It Does

- Identify conditions that may qualify for VA disability benefits
- Find secondary and presumptive claims you may have missed
- Understand the strengths and gaps in your evidence
- Prepare for C&P exams and doctor appointments
- Draft messages to your VSO, attorney, or VA representative
- Build buddy statements and impact statements that carry legal weight

It does not file claims, access your VA records, or provide legal advice. It helps you think through your claim more clearly.

---

## Every Citation Must Be Verified

Claim Scout generates case citations, CFR sections, and BVA decision references as part of its analysis. **Treat every one of them as unverified until you check it against eCFR, KnowVA, or the primary decision text.** The framework is instructed to flag citations it isn't confident about (look for `⚠️ LOW CONFIDENCE CITATION`), but a citation with no warning attached is not the same as a citation that's been checked — it means the model was confident, not that the citation is correct. A confidently-worded citation can still be wrong. Verify before you or your representative rely on any of them.

---

## How It Works

Three files ship. Your tracker is generated on first run — never shipped, never reused.

1. **START_HERE.md** — orientation. Read it once.
2. **Scout.md** — discovers potential claims, maps evidence links, identifies gaps, and runs threshold and pattern scans.
3. **Build_Evidence.md** — every evidence-building step, in order.

On your first run, the AI asks whether you already have a claim tracker. If you do, it writes there. If not, it generates `Tracker.md` for you from the schema in START_HERE.md — your data lives in your copy, nowhere else.

---

## Files

- `START_HERE.md` — start here
- `Scout.md` — discovery, gap analysis, threshold and pattern scans
- `Build_Evidence.md` — evidence-building steps in order
- `Requirements.md` — the numbered requirements this system is built against
- `Tracker.md` — not shipped; generated on your first run

---

## How to Use It

**Option 1 — Upload (easiest):** Upload `START_HERE.md` to any capable AI, then follow its steps.

**Option 2 — Paste:** Open `START_HERE.md` in any text editor, copy the full contents, and paste them into your AI chat as your first message.

No account required. No setup. No cost.

---

## Free and Open Source

Claim Scout is free to use, share, and build on. If you use it or adapt it, please link back so others can find it.

*License: MIT — see LICENSE.md.*

---

## Part of LLM Frameworks

Claim Scout is one plugin in the [LLM Frameworks](https://github.com/LLM-Frameworks) library — logic frameworks for evaluating claims, built to work against their author's own arguments.

---

## Disclaimer

Claim Scout is an AI prompt framework, not a law firm. Nothing it produces is legal advice. Always consult a VSO, accredited claims agent, or VA-accredited attorney before making decisions about your claim. File claims at VA.gov.
