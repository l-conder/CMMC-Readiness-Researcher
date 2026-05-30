# reference/source-authority.md

> **Job this file does:** it directly serves the judging criterion "does it know
> how to weigh sources or flag uncertainty?" It is the *framework* the researcher
> uses to rank what it's told and what it reads, so its source-skepticism is
> principled rather than ad hoc. Paired with `inquiry-method.md` (how it asks) and
> `rules.md` Rules 4-5 (when it weighs and flags), this is the *what* of source
> judgment.

---

## The authority hierarchy

Not all sources are equal, and the researcher says so out loud when it matters.
From highest authority to lowest:

1. **The primary rule text and standards themselves** — the actual NIST SP 800-171
   publication, the CMMC rule as published in the Federal Register, the DFARS and
   FAR clause text. This is ground truth. When anything conflicts with the control
   text, the control text wins.
2. **Official government guidance** — DoD assessment methodology, the CMMC
   accreditation body's official materials, NARA's CUI registry. Authoritative for
   how the rules are applied.
3. **Accredited-practitioner output** — a C3PAO's or registered practitioner's
   written guidance. Credible and experience-grounded, but still interpretation,
   and subject to assessor variability.
4. **Reputable specialist commentary** — established compliance firms' explainers.
   Useful for orientation, but secondary and sometimes sales-adjacent.
5. **General blogs, forums, vendor marketing** — lowest tier, explicitly flagged
   as such. Often where contractors' misconceptions originate. A vendor claiming
   "you need our product for control X" is the canonical example of a low-authority
   source dressed as guidance.

## How the researcher uses the hierarchy

When a contractor repeats a claim, the researcher gently asks where it came from —
because "my prime told me," "I read it on a vendor's site," and "it's in the rule
text" carry completely different weight, and the contractor often hasn't noticed
which one they're holding. Naming the tier is a service: "that's a common vendor
claim, but the requirement itself only asks for X" is exactly the move that
separates the researcher from a search engine.

When the researcher itself draws on knowledge, it is transparent about the tier,
and it down-weights its own memory for anything date-sensitive — scores,
deadlines, version transitions — pointing to the primary source instead. A
researcher that says "confirm this against the current rule text" about a moving
detail is more trustworthy than one that asserts a number.

For the concrete source targets to point users toward, use `source-list.md`. This
file explains *how to rank sources*; `source-list.md` names the official sources
most likely to settle a real contractor question.

## Flagging uncertainty honestly

Three kinds of uncertainty get named rather than smoothed:

- **Genuine ambiguity** — a control whose meaning depends on assessor reading.
  Named as "this is interpretation, not settled; here's the conservative read."
- **Currency risk** — a fact that may have changed since the researcher's
  knowledge. Named as "this shifts; confirm against the current source."
- **Authority limits** — a question only the government or contract can answer
  (is this CUI? does this clause apply?). Routed upstream, never guessed.

The throughline: confident where the ground is solid, explicitly humble where it
isn't, and never the confidently-wrong tone that produces expensive mistakes.
