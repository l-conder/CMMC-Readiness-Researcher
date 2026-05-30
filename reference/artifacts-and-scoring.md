# reference/artifacts-and-scoring.md

> **Job this file does:** it is the *key-concepts* reference for the three things
> an assessor demands — the System Security Plan, the Plan of Action & Milestones,
> and the SPRS score — plus the gap-weighing logic that tells the researcher which
> shortfalls are deferrable and which are hard stops. This is what makes Stage 4
> ("find the gap and weigh it") more than a checklist.

---

## The System Security Plan (SSP)

The SSP is the master document: it describes the system, defines the boundary, and
states how each requirement is met. The hard-won truth practitioners repeat is
that **you are, in an assessor's eyes, what your SSP says you are** — you define
your own scope and boundaries in it, and you are judged against what you wrote. A
strong SSP is thorough, has clearly defined boundaries, and for any inherited
control names the specific inheritance and the reference behind it.

For the researcher, the SSP is usually the central artifact a contractor needs to
build or fix, and "what does your SSP currently say about that?" is a frequent,
productive question. A vague SSP sinks an otherwise-secure company.

## The Plan of Action & Milestones (POA&M)

The POA&M lists requirements not yet met and the concrete plan — owners,
milestones, dates — to close them. The sharp, decision-driving nuance:

- **Some shortfalls can be POA&M'd** — documented as a plan and closed later,
  within a limited window.
- **Some cannot.** Certain critical controls must be fully in place at assessment
  time and are not eligible for a POA&M at all. Multifactor authentication and
  FIPS-validated encryption are the classic examples.
- There are generally **eligibility limits**: a minimum score is typically required
  before a POA&M is even allowed, and open POA&M items usually must be closed
  within a fixed period (commonly cited as 180 days). *These thresholds are exactly
  the kind of specific that the researcher should confirm against current official
  CMMC source material rather than assert from memory — they have shifted across
  rule versions.*

This deferrable-versus-hard-stop distinction is the heart of gap-weighing. When a
contractor names a gap, the researcher's instinct is: "is that one you can plan to
fix, or one that has to be done before anyone assesses you?"

## The SPRS score

SPRS (Supplier Performance Risk System) is the government system where a
self-assessment score is posted. The mechanics that matter:

- The score starts at a **maximum of +110** (all requirements met) and **weighted
  points are subtracted** for unmet requirements — not evenly. Some unmet controls
  cost 1 point, some 3, some 5, reflecting their security weight.
- Because deductions are weighted and numerous, the score can fall well below zero
  — as low as **-203**.
- A high score on paper does not guarantee passing a real assessment; it's a gate
  and a signal, not proof. Practitioners note self-assessed scores often come in
  far higher than what an assessor later validates, precisely because contractors
  miss where their CUI really lives.

The researcher treats the SPRS number as a conversation-starter, not a verdict:
"how was that score calculated, and which controls did you count as met?" is more
useful than the number itself.

## The senior-official affirmation

A named senior official must formally affirm the contractor's status in SPRS. This
carries personal and legal weight — a false affirmation has consequences under
laws governing false claims to the government. The researcher uses this to explain
*why* "close enough" is not a safe posture: someone has to put their name to it.

---

## How this powers Stage 4

Put together, these artifacts let the researcher do real gap-weighing rather than
list-reciting. A gap is assessed on three axes: is it a hard stop or
POA&M-eligible; how many SPRS points does it carry; and is it the kind of thing an
assessor reliably probes. A researcher that can say "that one's a hard stop, it
can't be deferred, and it's a high-point control — so it belongs at the top of
your list" is doing the thing a summarizer never could.
