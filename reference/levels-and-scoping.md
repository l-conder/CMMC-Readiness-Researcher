# reference/levels-and-scoping.md

> **Job this file does:** it is the *framework* that turns the first three stages
> of the investigation into a decision. `rules.md` says "establish the data, map
> where it lives, then establish the obligation" — this file is the logic that
> connects those answers to a level and a boundary. It is the researcher's
> internal decision tree, written as notes, not as user-facing speech.

---

## The data-to-level logic (Stage 1 -> Stage 3)

Everything starts with the data, because the data decides the level, and the level
decides the work. The logic, in order:

1. **Does the contractor handle Federal Contract Information (FCI) only?** If the
   work involves non-public information generated under a federal contract, but no
   Controlled Unclassified Information, the obligation is **Level 1**: the 15 basic
   safeguarding requirements from FAR 52.204-21, assessed by the contractor itself,
   annually. This is the short road.

2. **Does the contractor handle Controlled Unclassified Information (CUI)?** If so,
   the obligation is **Level 2**: all 110 NIST SP 800-171 Rev 2 requirements. This
   is the heavy road, and most of the researcher's work lives here.

3. **Is the program among the most sensitive (high-value assets, critical
   programs)?** A small subset reaches **Level 3**: the Level 2 baseline plus a
   selected set of enhanced requirements drawn from NIST SP 800-172, assessed by
   the government (DIBCAC), not a commercial assessor. Rare for small contractors,
   but the researcher should know it exists so it never overstates the common case.

The researcher never asserts the level on its own authority. The binding driver is
the contract and the government customer's CUI determination. The researcher's job
is to help the contractor reason to the *likely* answer and to the right question
for their contracting officer.

## Who assesses Level 2 (the fork inside the fork)

Level 2 is not one path. Whether a contractor self-assesses or must bring in a
third party depends on how the contract is prioritized:

- **Self-assessment** path: the contractor performs its own annual assessment and
  posts the result. Lower cost, faster, but the senior-official affirmation puts
  real accountability on a named executive.
- **Third-party (C3PAO)** path: an accredited outside assessor conducts the
  certification. Higher cost, scheduling lead time (assessor slots are limited),
  and a harder bar.

Which path applies changes the contractor's timeline and budget dramatically, so
once Level 2 is established, "self or third-party?" is the immediate next question
— and again, it traces to the contract, not to the tool.

---

## The scoping logic (Stage 2, the highest-value move)

Scoping defines the *assessment boundary* — the set of assets evaluated against
the requirements. Getting it right is the single biggest lever on cost and
outcome: scope too wide and the contractor remediates systems that never needed
it; scope too narrow and CUI hides in an unscoped system and the assessment fails.

The researcher silently sorts every asset a contractor mentions into categories.
The working categories to reason with:

- **CUI Assets** — anything that stores, processes, or transmits CUI. Squarely in
  scope, fully assessed.
- **Security Protection Assets (SPAs)** — things that protect the CUI assets:
  firewalls, identity systems, logging/SIEM, the management plane. In scope,
  because if they fail, the protection fails.
- **Contractor Risk Managed Assets** — assets that *could* reach CUI but are
  managed by policy not to. In scope to a degree, and a common gray area worth
  probing.
- **Specialized Assets** — things like IoT, OT, test equipment, government-furnished
  equipment that need handling but may be assessed differently.
- **Out-of-Scope Assets** — genuinely segregated from CUI, with no path to it.
  Out, *if* the separation is real and demonstrable.

The recurring trap: a contractor calls an asset out-of-scope because they *intend*
it to be, but there's an undocumented path — a shared login, an email forward, a
synced drive — that quietly pulls it back in. The researcher's scoping questions
exist to find those paths before an assessor does.

## The enclave strategy

The most effective scope-reduction move is often an **enclave**: deliberately
isolating CUI into a bounded, hardened environment so the assessment boundary is
small and clean, rather than letting CUI sprawl across the whole company. When a
contractor's CUI touches everything, the researcher's instinct is to ask whether
the work could be concentrated into an enclave — turning a company-wide assessment
into a contained one. This is strategy, not paperwork, and it's where a sharp
scoping conversation saves the most money.
