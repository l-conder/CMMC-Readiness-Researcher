# reference/glossary.md

> This is not a vocabulary list. A summarizer defines terms; a researcher knows
> how they *relate* — who decides what, where data can safely live, what's a hard
> stop versus what's deferrable. Each entry below gives the plain meaning and then
> the thing that actually matters: why this term changes a decision in the
> investigation. Read it that way, and the acronyms stop being noise and become a
> map of the terrain.
>
> When an exact figure or current rule is involved, treat the dedicated framework
> files in this folder as the source of record, and the authoritative government
> publication above that. Microsoft-specific product details below are described
> at a working level and should be confirmed against current Microsoft
> documentation, because product capabilities change.

---

## The frameworks and standards

**NIST SP 800-171** — The National Institute of Standards and Technology
publication that lists the security requirements for protecting sensitive
government information when it lives on a contractor's own systems rather than the
government's. This is the *recipe*. Revision 2 is the working baseline today (110
requirements, 14 families). Revision 3 exists and is the direction of travel but
is not yet what you're assessed against. *Why it matters:* this is the document
the entire obligation is built on. When in doubt, the control text here outranks
anyone's summary of it, including this researcher's.

**NIST SP 800-172** — A companion publication of *enhanced* requirements that go
beyond 800-171, used for the most sensitive contracts. *Why it matters:* it's the
source of the extra controls at the highest CMMC level, so it only enters the
conversation for contractors handling the most critical programs.

**NIST SP 800-53** — The giant master catalog of security controls for the
government's own systems. 800-171 is a tailored subset carved out of it. *Why it
matters:* mostly context — it explains where 800-171's controls came from, and
occasionally a contractor will encounter it through a cloud provider's
documentation.

**CMMC** — Cybersecurity Maturity Model Certification. The Department of Defense's
program for *verifying* that a contractor actually meets the 800-171 recipe. CMMC
is the *inspection badge*, not a new recipe. *Why it matters:* this is the thing
with the deadline and the assessment. It's why a contractor is in your chair.

**FAR 52.204-21** — The Federal Acquisition Regulation clause that lists the 15
basic safeguarding requirements for Federal Contract Information. *Why it
matters:* this is the source of the Level 1 obligation — the short list. If a
contractor only handles FCI, this clause, not the 110 controls, is their world.

**DFARS 252.204-7012 / -7019 / -7020 / -7021** — The Defense Federal Acquisition
Regulation Supplement clauses that impose CUI protection, self-assessment
reporting, and the CMMC requirement on defense contracts. *Why it matters:* these
are the contractual hooks that make any of this mandatory. When a contractor asks
"do I really have to?", the answer lives in which of these clauses is in their
contract — which is a question for their contracting officer, not for this tool to
decide.

---

## The two kinds of data (the fork that decides everything)

**FCI — Federal Contract Information** — Information provided by or generated for
the government under a contract, not intended for public release, but not
especially sensitive. *Why it matters:* FCI alone triggers only the 15 basic
safeguards (Level 1). Establishing that a contractor handles FCI and *only* FCI
can save them an enormous amount of unnecessary work.

**CUI — Controlled Unclassified Information** — The sensitive category:
information the government requires to be protected or controlled, though it isn't
classified. *Why it matters:* CUI is the trigger for the full 110 requirements
(Level 2) and third-party assessment. The single most consequential question in
the entire investigation is whether the contractor handles CUI, and the binding
answer comes from the contract and the government customer, never from the
contractor's guess.

---

## The levels and who assesses them

**Level 1 (L1)** — The foundational tier: 15 basic safeguards for FCI, assessed by
the contractor itself, annually. *Why it matters:* it's the floor, and it's
self-attested, so the stakes and effort are far lower.

**Level 2 (L2)** — The tier most defense contractors care about: all 110 NIST
800-171 Rev 2 requirements, for CUI. Assessment is either a self-assessment or a
third-party assessment depending on how the contract is prioritized. *Why it
matters:* this is the heavy lift, and whether you self-assess or need a C3PAO
changes your cost and timeline dramatically.

**Level 3 (L3)** — The highest tier: the Level 2 baseline plus a selected set of
enhanced requirements from 800-172, government-assessed, for the most sensitive
programs. *Why it matters:* rare for small contractors, but knowing it exists
keeps the researcher from overstating what most contractors face.

---

## The people (who decides what)

**OSC — Organization Seeking Certification** — The contractor being assessed; the
company in the chair. *Why it matters:* it's the role your user occupies, and the
term shows up constantly in official guidance.

**C3PAO — Certified Third-Party Assessment Organization** — The accredited
outside organization authorized to conduct CMMC Level 2 certification
assessments. *Why it matters:* this is who confers certification — not this tool,
not the contractor. The researcher prepares a contractor *for* the C3PAO and
always routes the binding judgment there. Note also: C3PAOs assess against Rev 2,
not Rev 3.

**Prime / Prime Contractor** — The company holding the contract directly with the
government. *Why it matters:* the Prime flows the CMMC requirement *down* to its
subcontractors. This flow-down is the usual reason a small contractor suddenly has
to comply — they got a letter from their Prime, not from the DoD directly.
Understanding this explains the panic that often brings a contractor to the
researcher in the first place.

**COR — Contracting Officer's Representative** (and **CO — Contracting Officer**)
— The government-side people who manage the contract and make official
determinations about it. *Why it matters:* questions the researcher cannot answer
with authority — does this contract involve CUI, does this clause apply — route to
the CO/COR. They make the binding call.

**DIB — Defense Industrial Base** — The entire ecosystem of companies that supply
the DoD, from giant primes to one-person shops. *Why it matters:* it's the
researcher's whole audience, and the reason the requirements cascade so widely —
the DoD is securing the supply chain, not just individual firms.

---

## The artifacts (what an assessor demands)

**SSP — System Security Plan** — The master document describing how the contractor
meets each requirement, what's in scope, and where the boundaries sit. A
practitioner's hard-won truth: *you are what's in your SSP* — you define your own
boundaries and scope, and an assessor judges you against what you wrote. *Why it
matters:* this is the central artifact. A vague or sloppy SSP sinks an assessment
regardless of how good the underlying security is.

**POA&M — Plan of Action & Milestones** (verbed by practitioners as "POA&M'd") —
The document listing requirements not yet met and the concrete plan, with dates
and owners, to close them. *Why it matters, and this is a sharp one:* some
non-critical controls can be POA&M'd and finished later, but certain critical
controls — FIPS-validated encryption, multifactor authentication, and core access
control among them — *cannot* be deferred; they must be fully in place at
assessment time. The researcher's gap-weighing depends on knowing which gaps are
deferrable and which are hard stops.

**SPRS — Supplier Performance Risk System** — The government system where a
contractor posts its self-assessment score. *Why it matters:* the score is often
the first thing a Prime or the DoD looks at. The scoring runs from a maximum of
+110 down into the negatives (as low as -203), because unmet controls carry
weighted point deductions of differing severity. A high score on paper still has
to survive a real assessment — the number is a gate, not a guarantee.

**Assessment Objectives** — The granular sub-points an assessor checks; the 110
requirements expand into a larger set of these (320 objectives). *Why it matters:*
it's why "we did the 110 controls" isn't the whole story — each control has
specific things that must be demonstrably true, and the SSP has to speak to them.

---

## Where CUI can safely live (the environment terms)

**Enclave** — A deliberately bounded, hardened environment that holds CUI and
keeps it separated from the rest of the business. *Why it matters:* scoping a tight
enclave, rather than dragging the whole company into the assessment boundary, is
one of the biggest levers for reducing cost and effort. This is exactly the
scope conversation in Stage 2 of the investigation.

**GCC High — Government Community Cloud High** — Microsoft's government-focused
cloud, built to meet the elevated requirements for CUI (and aligned to FedRAMP
High). *Why it matters:* it's a common, credible home for CUI, and it connects
directly to the data-handling boundary in the rules — a FedRAMP-authorized
environment is *where* controlled data is allowed to live, unlike a general
commercial tool.

**Inheritance** — When a cloud provider already satisfies a control on your
behalf, so you "inherit" it rather than building it yourself. On GCC High a large
share of controls can be fully or partially inherited. *Why it matters, with a
caveat practitioners insist on:* inheritance is the single biggest time-saver, but
*inherited does not mean done* — partial inheritance still requires the contractor
to document their own side. The researcher should celebrate inheritance and warn
against assuming it.

**Appendix J / CMMC Implementation Guide** — Microsoft's documentation of what's
inherited (Appendix J) and how its technology satisfies each control (the
Implementation Guide). *Why it matters:* these are the practical resources a
GCC High contractor lives in. Knowing they exist marks the researcher as someone
who's actually been in the work.

**Intune / Conditional Access / MAM / BYOD** — Microsoft's device management
(Intune), policy enforcement based on conditions like user, device, and location
(Conditional Access), Mobile Application Management that keeps CUI inside approved
apps (MAM), and Bring Your Own Device arrangements. *Why it matters:* these are the
real mechanisms that enforce many controls in a Microsoft environment, and BYOD
via MAM is a known assessor focus area — not a checkbox. The researcher doesn't
configure these, but recognizing them keeps the conversation grounded in how the
work actually gets done.

**Sentinel / KQL** — Microsoft's security information and event management tool
(Sentinel) and its query language (KQL), used to satisfy logging and monitoring
requirements. *Why it matters:* logging is a whole control family, and "we turned
on Sentinel" is not the same as a working logging story — data connectors,
retention, and permissions all have to be right. Recognizing this prevents the
researcher from accepting a tool's *presence* as evidence of a control's
*function*.

**VDI — Virtual Desktop Infrastructure** — Remote virtual desktops (for example,
AWS WorkSpaces) sometimes used to contain CUI. *Why it matters:* it's one
architectural choice among several for keeping data in-boundary, with real
tradeoffs in user experience and the risk that users route around it — a scoping
consideration, not a default answer.

**OOBE — Out-Of-Box Experience** — The initial setup flow when a new machine is
first turned on, often automated for enrolled devices. *Why it matters:* mostly
operational, but it surfaces in real migrations as a place where "the vendor said
it was configured" and "it actually worked" diverge — a reminder to verify rather
than trust.

---

## The rollout clock

**Phase 1 / Phased Rollout** — CMMC is being introduced in phases rather than all
at once, with self-assessment obligations arriving before full third-party
certification requirements. *Why it matters:* the phase a contract falls under
determines whether a contractor can self-attest for now or already needs a C3PAO.
"We'll deal with it later" stopped being viable once the phases began landing on a
fixed calendar — and the exact dates are the kind of thing to confirm against
current official sources, since they drive real deadlines.

---

## More terms a contractor will actually say (expanded bridge)

The entries below extend the bridge. A contractor rarely speaks in clean
textbook terms — they say "our DIBCAC score" or "we're a COTS vendor" or "is this
an SPA or a CSP question." The researcher needs to parse these on contact and
answer in the same vocabulary, without making the person feel they used the wrong
word. Each entry keeps the same shape: plain meaning, then the decision it
touches.

**Cyber-AB / The Cyber AB** — The accreditation body that oversees the CMMC
ecosystem of assessors and training. *Why it matters:* it's the source of who is
and isn't a legitimate C3PAO or registered practitioner. When a contractor asks
"is this consultant real," the answer traces back to Cyber-AB accreditation.

**RPO — Registered Provider Organization / RP — Registered Practitioner** — Firms
and individuals registered to provide CMMC *consulting* (advice and prep), as
distinct from the C3PAO that *assesses*. *Why it matters:* an RPO helps you get
ready; it cannot certify you. Contractors routinely conflate the two, and the
distinction affects who they should hire for what. The researcher itself sits in
the "prep" world, not the "assess" world — same boundary.

**DIBCAC — Defense Industrial Base Cybersecurity Assessment Center** — The
government body that conducts high-level assessments, including Level 3 and certain
high-stakes Level 2 reviews. *Why it matters:* a DIBCAC assessment is a different
animal from a C3PAO assessment, and "DIBCAC-validated" carries particular weight.
If a contractor mentions DIBCAC, the stakes and rigor just went up.

**Assessor variability** — The practitioner-observed reality that two assessors can
read the same control differently and grade the same evidence differently. *Why it
matters:* it's the lived reason behind Rule 5 on flagging ambiguity. The researcher
should never promise "an assessor will accept this" — only "here's the
conservative reading most assessors expect," because the next assessor may differ.

**COTS — Commercial Off-The-Shelf (and the COTS exemption)** — Standard commercial
products sold to the public without modification. Some pure-COTS resellers may not
handle CUI at all and can fall outside the heavier requirements. *Why it matters:*
it's a genuine off-ramp for the right kind of company — establishing whether a
contractor is "just reselling COTS" can change their entire obligation, which is
exactly the kind of framing question the researcher exists to surface.

**CUI Categories / CUI Registry / CUI marking** — CUI is not one undifferentiated
blob; the National Archives maintains a registry of CUI categories, and properly
marked CUI carries specific labels. *Why it matters:* whether information is
*actually* CUI — and whether it was *marked* as such by the government — is central
to scoping, and the responsibility for marking generally sits with the government
or the prime, not the receiving contractor. The researcher routes the binding call
upstream while helping the contractor reason about likelihood.

**SPA — Security Protection Asset** and **CUI Asset / In-scope vs. out-of-scope
assets** — In CMMC scoping, assets are categorized by their relationship to CUI:
assets that handle CUI, assets that *protect* those assets (firewalls, SIEM,
identity systems — the SPAs), and assets genuinely out of scope. *Why it matters:*
this categorization *is* the scoping exercise from Stage 2. Getting an asset's
category wrong is how scope balloons or springs a leak. When a contractor lists
their systems, the researcher is silently sorting them into these buckets.

**ESP / MSP — External Service Provider / Managed Service Provider** — Outside
companies that run part of a contractor's IT or security. *Why it matters:* if an
ESP touches CUI or the systems that protect it, the ESP's own security folds into
the contractor's assessment scope. A contractor who says "oh, our MSP handles all
that" has just named a major scoping question, not closed one.

**Shared Responsibility Model** — The principle that in any cloud arrangement,
some controls are the provider's job and some are the customer's, with a line
between them that varies by service. *Why it matters:* it's the formal name for the
"inherited does not mean done" trap. The researcher uses it to ask *where exactly*
the line falls for this contractor's setup, rather than letting "the cloud handles
it" stand.

**FIPS-validated encryption** — Encryption that meets a specific federal validation
standard (FIPS 140). *Why it matters, and it's a sharp one:* for CUI, encryption
generally must be FIPS-*validated*, not merely "strong" or "AES-256." Plenty of
contractors believe they're covered because they encrypt, then learn their
encryption isn't validated. And recall this is a control that typically cannot be
deferred on a POA&M — it's a hard stop. A prime candidate for an investigative
question.

**MFA — Multifactor Authentication** — Requiring more than a password to
authenticate. *Why it matters:* it's both one of the most cited controls and one of
the critical ones that must be fully implemented at assessment time, not
POA&M'd. Its presence or absence is an early tell about how far along a
contractor really is.

**Affirmation (Senior Official Affirmation)** — A required step where a senior
company official formally attests, in SPRS, to the contractor's compliance status.
*Why it matters:* it puts personal accountability on a named executive and carries
real legal weight (false attestations have consequences). It's why "good enough"
isn't a posture a contractor can afford — someone has to sign their name to it.

**FedRAMP — and FedRAMP "equivalency" / "Moderate" / "High"** — The federal program
that authorizes cloud services at impact levels (Moderate, High). *Why it matters:*
a cloud service that stores or processes CUI generally needs to be FedRAMP
Moderate (or meet an equivalency bar), and this is the same authorization concept
behind the data-handling boundary in `rules.md`. When a contractor names a SaaS
tool that touches CUI, "is it FedRAMP authorized at the right level?" is the
immediate question.

**320 Assessment Objectives** — The 110 requirements expand into 320 discrete,
checkable objectives an assessor evaluates. *Why it matters:* it's the gap between
"we did the control" and "we can demonstrate every sub-part of the control." A
researcher uses it to push past surface confidence: meeting a control means
meeting *all* its objectives, with evidence.
