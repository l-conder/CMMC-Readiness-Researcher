# The CMMC Readiness Researcher

**A folder-based AI research partner for small defense contractors facing CMMC /
NIST SP 800-171.** Drop it into a Claude Project and Claude becomes a readiness
researcher that investigates your situation before it tells you anything — because
in compliance, the wrong answer delivered confidently is more dangerous than no
answer at all.

> **One thing up front, so you can relax:** this researcher never needs your actual
> sensitive data. It works on the *type* of information you handle and *where it
> lives* — not its contents. Don't paste anything controlled (CUI) into it; a
> general-purpose AI tool isn't an authorized environment for that, and the
> researcher will stop you and explain why if you try. The shape of your
> environment is all it needs, and none of that is controlled information.

---

## The one distinction that governs everything

**A researcher investigates. A summarizer recites.**

Hand most AI tools the word "CMMC" and they print the 110 controls of NIST
800-171. That answer is worse than useless, because it skips the one fact that
decides your entire obligation: *what kind of government data do you actually
handle?* Handle only Federal Contract Information and you may owe 15 basic
safeguards; handle Controlled Unclassified Information and you are likely in the
Level 2 world of 110 NIST SP 800-171 requirements, with the assessment path
depending on the contract. A control list handed over before that's settled sends
you to climb the wrong mountain.

This researcher refuses to do that. It asks before it answers, weighs your sources
against the rule text, flags what's genuinely uncertain instead of faking
confidence, and — this is the whole point — asks the questions you didn't know to
ask yourself.

---

## How to use it (cold, in five minutes)

1. **Create a new Claude Project.**
2. **Paste `PROJECT_INSTRUCTIONS.md` into the project instructions.** That gives
   Claude the load order, safety boundaries, and response contract.
3. **Add these files to the project's knowledge.** The whole folder. Start a
   conversation and the researcher is live — no setup, no prompt-engineering on
   your end.
4. **Tell it your situation in plain language.** "A prime told us we need CMMC for
   a contract and I don't know where to start" is a perfect opening. So is "we
   handle some drawings for a Navy program and I'm not sure if that's CUI."
5. **Expect questions back, not a checklist.** It will ask what data you handle,
   where it lives, and who touches it — one question at a time, with the reason
   attached — before it says anything about controls or levels. That's the design
   working, not the tool stalling.
6. **Use the closing summary.** At the end of an investigation it pulls together a
   readiness picture — your likely data type, your scope boundary, your likely
   level, your top gaps, and your next concrete step — that you can carry into a
   conversation with a real assessor or your contracting officer.

If you only do one thing: describe your actual situation and let it interrogate
it. The value is in the questions.

---

## What's in the folder, and why

The build separates what never changes (the researcher's character and knowledge)
from what changes every conversation (what it learns about you). That separation
is the methodology — Interpretable Context Methodology — made visible.

**The character (fixed — this is *who the researcher is*):**

- `PROJECT_INSTRUCTIONS.md` — paste this into Claude Project instructions so the
  folder loads with the intended behavior and safety boundaries.
- `identity.md` — who the researcher is, what it covers, and the hard edges of
  what it refuses to do.
- `rules.md` — the engine: the five-stage investigative sequence, the data-handling
  boundary, the source-weighing and uncertainty rules. How it behaves, turn by
  turn.
- `examples.md` — three before-and-after interactions showing the summarizer's
  wrong answer beside the researcher's right one. Voice and behavior, demonstrated.
- `JUDGE_GUIDE.md` — adversarial prompts and pass/fail criteria for testing
  whether the folder really investigates.
- `SPEC.md` — the build spec for an optional interactive web demo that proves the
  folder's behavior without replacing it.

**The knowledge (fixed — this is *what the researcher knows*), in `reference/`:**

- `inquiry-method.md` — the evidence-based investigative-interviewing framework
  (OARS, information-gathering over accusatorial) that governs *how* it asks.
- `glossary.md` — the domain's acronyms and concepts, each wired to the decision it
  affects, so the researcher speaks the contractor's language fluently.
- `levels-and-scoping.md` — the decision logic from data type to level to
  assessment boundary.
- `artifacts-and-scoring.md` — the SSP, POA&M, and SPRS, plus which gaps are hard
  stops and which can be deferred.
- `rev2-vs-rev3.md` — the single most important "check the date, weigh the source"
  lesson in the domain.
- `source-authority.md` — how the researcher ranks what it's told and flags what's
  uncertain.
- `source-list.md` — the official sources the researcher points users back to when
  a deadline, clause, score, or assessment path needs current confirmation.
- `common-failure-modes.md` — the recurring traps the researcher actively looks
  for: email CUI, MSP scope, Rev. 3 confusion, tool shortcuts, weak evidence.
- `readiness-artifacts.md` — safe output shapes for intake summaries, scope maps,
  source-weighing notes, evidence gaps, and readiness snapshots.

**The variable layer (changes every conversation — this is *what it learns about
you*):**

- `reference/intake.md` — the bounded, per-engagement scratchpad of your specific
  situation. Kept small on purpose, so situational detail never crowds out the
  researcher's character.

---

## What this researcher is honest about

It is a thinking aid, and it says so. **It does not certify anyone** — only an
accredited C3PAO or the government does that. **It does not give legal advice** on
contract terms or clauses. **It does not make the binding CUI determination** —
that comes from your contract and your government customer; the researcher helps
you reason toward the right question to ask them. And it works only on the *shape*
of your environment, **never on actual controlled information** — don't paste CUI
into it, because a general-purpose AI tool isn't an authorized environment for
controlled data, and it will stop you and explain why if you try.

These aren't limitations bolted on at the end. They're the reason the researcher
can be trusted: it knows the edge of its own competence and routes you to the
right human when you reach it.

**If you genuinely need AI on real controlled data**, there is a compliant route —
but it isn't a tool like this one. It's a FedRAMP-authorized deployment (for
example, a government-authorized cloud environment), which comes with the real
tradeoff that the model versions available inside those boundaries often lag the
newest commercial ones. This researcher is for *readiness reasoning*, not for
handling CUI — and knowing the difference is part of the point.

---

## A note on currency

CMMC and NIST 800-171 are a moving target — phase dates, scoring thresholds, and
the Rev 2 to Rev 3 transition all evolve. This folder reflects the landscape as of
early 2026 and is built to *flag* date-sensitive facts and point you to the
authoritative source rather than assert a number that may have shifted. When a
detail drives a real deadline or dollar, confirm it against the current NIST and
official CMMC publications. The researcher will tell you when you're in that
territory.
