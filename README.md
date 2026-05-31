# Quaesitor
# The CMMC Readiness Researcher

> ### 👉 [Try the live demo](https://l-conder.github.io/CMMC-Readiness-Researcher/) — no signup, no install
> Click a scenario and watch the researcher *investigate* instead of reciting a checklist:
> it refuses to dump the 110 controls, catches a "we need Rev 3" vendor trap, and stops a
> controlled-data paste cold — while a live panel shows its reasoning the whole way.
> **The folder is the brain; the demo is a viewer over it.**


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
Level 2 world of 110 NIST SP 800-171 requirements, with the assessment path —
self-assessment or third-party certification — depending on the contract. A
control list handed over before that's settled sends you to climb the wrong
mountain.

This researcher refuses to do that. It asks before it answers, weighs your sources
against the rule text, flags what's genuinely uncertain instead of faking
confidence, and — this is the whole point — asks the questions you didn't know to
ask yourself.

---

## How to use it (cold, in five minutes)

1. **Create a new Claude Project.**
2. **Add these files to the project's knowledge.** The whole folder. Start a
   conversation and the researcher is live — no setup, no prompt-engineering on
   your end.
3. **Tell it your situation in plain language.** "A prime told us we need CMMC for
   a contract and I don't know where to start" is a perfect opening. So is "we
   handle some drawings for a Navy program and I'm not sure if that's CUI."
4. **Expect questions back, not a checklist.** It will ask what data you handle,
   where it lives, and who touches it — one question at a time, with the reason
   attached — before it says anything about controls or levels. That's the design
   working, not the tool stalling.
5. **Use the closing summary.** At the end of an investigation it pulls together a
   readiness picture — your likely data type, your scope boundary, your likely
   level, your top gaps, and your next concrete step — that you can carry into a
   conversation with a real assessor or your contracting officer.

If you only do one thing: describe your actual situation and let it interrogate
it. The value is in the questions.

---

## What's in the folder, and why

```
cmmc-readiness-researcher/
├── PROJECT_INSTRUCTIONS.md     # Layer 0 — load first: order, boundaries, response contract
├── identity.md                 # Character — who the researcher is, and won't be
├── rules.md                    # Engine — the 5-stage investigative sequence, turn by turn
├── examples.md                 # Demonstrated behavior — summarizer (wrong) vs researcher (right)
├── JUDGE_GUIDE.md              # Adversarial prompts + pass/fail criteria
├── SPEC.md                     # Build spec for the optional web demo
├── README.md                   # You are here
├── reference/                  # Knowledge (fixed) + the variable layer
│   ├── inquiry-method.md       #   how it asks — OARS / information-gathering framework
│   ├── glossary.md             #   acronyms wired to the decision each one affects
│   ├── levels-and-scoping.md   #   data type → level → assessment boundary
│   ├── artifacts-and-scoring.md#   SSP, POA&M, SPRS; hard stops vs deferrable gaps
│   ├── rev2-vs-rev3.md         #   the "check the date, weigh the source" lesson
│   ├── source-authority.md     #   how it ranks sources and flags uncertainty
│   ├── source-list.md          #   official sources to confirm against
│   ├── common-failure-modes.md #   the traps it actively probes for
│   ├── readiness-artifacts.md  #   safe output shapes (snapshot, scope map, etc.)
│   └── intake.md               #   VARIABLE layer — per-conversation scratchpad (~800 tokens)
└── docs/
    └── index.html              # The demo web app (served via GitHub Pages)
```


The build separates what never changes (the researcher's character and knowledge)
from what changes every conversation (what it learns about you). That separation
is the methodology — Interpretable Context Methodology — made visible.

**The character (fixed — this is *who the researcher is*):**

- `identity.md` — who the researcher is, what it covers, and the hard edges of
  what it refuses to do.
- `rules.md` — the engine: the five-stage investigative sequence, the data-handling
  boundary, the source-weighing and uncertainty rules. How it behaves, turn by
  turn.
- `examples.md` — three before-and-after interactions showing the summarizer's
  wrong answer beside the researcher's right one. Voice and behavior, demonstrated.

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
