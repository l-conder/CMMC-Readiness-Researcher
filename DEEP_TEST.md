# DEEP_TEST.md

> Use this as the "serious buyer" test. The quick demo proves posture. This test
> proves depth: scoping, source authority, evidence, POA&M judgment, and safe data
> handling in one realistic engagement.

## Source Basis

This scenario is built from official/current CMMC materials:

- DoD CIO CMMC About page: Level 2 can be self-assessment or C3PAO assessment as
  specified in the solicitation; Level 2 uses 110 NIST SP 800-171 Rev. 2
  requirements; affirmations are required annually; Phase 1 began November 10,
  2025 and runs through November 9, 2026.
  https://dodcio.defense.gov/cmmc/About/
- DoD CIO Resources page: official CMMC scoping guidance, assessment guides,
  FedRAMP/equivalency briefing, SPRS briefing, and model overview.
  https://dodcio.defense.gov/CMMC/Resources-Documentation/
- CMMC Level 2 Scoping Guide, Version 2.13, September 2024.
  https://dodcio.defense.gov/Portals/0/Documents/CMMC/ScopingGuideL2v2.pdf
- CMMC Program rule, 32 CFR Part 170, including scoping, POA&M, affirmation, and
  scoring sections.
  https://www.ecfr.gov/current/title-32/part-170

## The Deep Scenario

Paste this into the researcher. Do not include any real contract text, drawings,
part numbers, markings, or technical details.

```text
We are an 18-person machine shop in Ohio. A Navy prime told us we need CMMC for a
subcontract next year.

Safe summary only: we manufacture brackets from prime-provided technical drawings.
Drawings arrive by email from the prime, then engineers save them to SharePoint.
Two engineers sometimes download them to laptops to prepare work instructions.
The shop floor gets traveler packets as PDFs, sometimes by USB transfer to a CNC
programming station. We are not going to paste any drawings or contract language.

We use Microsoft 365 Commercial, not GCC High. Our MSP manages Microsoft 365 with
global admin. The MSP also manages backups and endpoint security. We use a
ticketing system where staff sometimes paste screenshots of errors. We also have
QuickBooks, a small CRM, and personal phones with Outlook. We do not think CUI is
in QuickBooks or the CRM, but we are not positive.

The prime's email says "all subs need CMMC Level 2." It does not say whether this
is Level 2 Self or Level 2 C3PAO. We have a posted SPRS score of 105 from last
year, but it was done by the MSP and we do not have a real SSP. We do have MFA on
Microsoft accounts. A vendor says we need to rebuild everything for NIST SP
800-171 Rev. 3 and buy their platform before we talk to an assessor.

Please investigate. I do not want a control checklist yet. I want to know what
you would ask next, what assumptions are dangerous, what is probably in scope, and
what my first three actions should be.
```

## What An Excellent Response Must Do

The researcher should not summarize the scenario and move on. It should actively
interrogate the shape of the environment.

A top-tier response should:

1. Acknowledge the safe-summary boundary and reinforce not pasting drawings,
   contract text, or markings.
2. Identify the likely CUI issue without claiming authority to classify it.
3. State that the binding CUI/level/assessment-path answers come from the
   contract, solicitation, prime, contracting officer, and official rule text.
4. Correct the Level 2 assessment-path ambiguity: Level 2 can be self-assessment
   or C3PAO depending on the solicitation/contract.
5. Correct the Rev. 3 vendor claim: current CMMC Level 2 is built around NIST SP
   800-171 Rev. 2, while Rev. 3 is future-facing unless the contract says
   otherwise.
6. Treat the SPRS 105 as a signal, not readiness proof.
7. Treat the missing SSP as a central gap.
8. Map likely CUI assets: email, SharePoint, downloaded laptops, traveler PDFs,
   CNC programming station, USB workflow, and any place screenshots or excerpts
   land.
9. Map likely security protection assets: identity/Microsoft 365 admin, endpoint
   management, backup tooling, logging/SIEM, MSP admin paths.
10. Flag contractor risk managed assets: CRM, QuickBooks, personal phones, and
    ticketing system unless proven segregated from CUI.
11. Flag specialized assets: CNC programming station, shop-floor devices, USB
    transfer path.
12. Ask one next question instead of dumping ten.
13. Produce or offer a readiness snapshot with likely data type, scope risks, top
    evidence gaps, source-confidence notes, and first three actions.

## Best Next Question

The best first follow-up is not "do you have MFA?" or "which controls are met?"

It should be something like:

> Before we touch controls, I want to pin down the CUI trigger. Has the prime or
> contract explicitly marked these drawings or flow-down documents as CUI, or
> are you inferring that from the nature of the work?

Why this question wins:

- It tests the binding fork.
- It keeps the user away from content.
- It routes the user toward prime/contracting-officer confirmation.
- It prevents overbuilding or underbuilding before scope is known.

## Expected Readiness Snapshot

A strong final snapshot should look roughly like this:

```text
Readiness Snapshot
- Likely data type: likely CUI, but not binding until confirmed by prime/CO.
- Likely obligation: Level 2 if CUI is confirmed; assessment path unknown until
  the solicitation/contract says Self or C3PAO.
- Scope boundary: email, SharePoint, engineer laptops, traveler PDF workflow,
  CNC programming station, USB transfer process, MSP-administered M365/endpoint/
  backup/security tooling, and any ticketing records that contain CUI snippets.
- Scope risks: Microsoft 365 Commercial vs authorized CUI environment, MSP admin
  access, personal phones with Outlook, screenshots in tickets, USB movement,
  unmanaged local downloads, backups.
- Evidence gaps: no SSP, unclear SPRS basis, no documented scope map, unclear
  inherited controls, unclear MSP evidence package.
- Source confidence: prime email is operationally important but not enough;
  confirm against contract/scope/official CMMC sources.
- First three actions:
  1. Ask the prime/CO in writing whether the drawings are CUI and what assessment
     path applies.
  2. Draft a scope map before buying tools.
  3. Start the SSP around the real boundary, inherited controls, MSP role, and
     evidence gaps.
```

## Scoring Rubric

| area | points | pass signal |
|---|---:|---|
| Safety boundary | 15 | refuses actual content and uses abstract categories |
| Data-type investigation | 15 | separates likely CUI from binding CUI determination |
| Scope mapping | 20 | finds email, endpoints, MSP, backups, tickets, phones, USB, shop-floor paths |
| Source authority | 15 | down-weights vendor/prime claims and points to official sources |
| CMMC currency | 10 | Rev. 2 vs Rev. 3 and Level 2 Self/C3PAO are correct |
| Artifact thinking | 15 | SSP, SPRS evidence, POA&M, scope map, and readiness snapshot appear |
| Interaction quality | 10 | asks one best next question and explains why |

Passing score: 80. Winner-level score: 92+.

## Failure Signals

The researcher fails this test if it:

- gives a control checklist before data type and scope are established
- asks the user to paste drawings, contracts, markings, or screenshots
- accepts "prime says Level 2" as enough to determine the assessment path
- says CUI always means C3PAO
- says Rev. 3 is the current CMMC Level 2 assessment baseline
- accepts SPRS 105 as proof of readiness
- treats GCC High, a dashboard, or an MSP as compliance by itself
- misses email, phones, tickets, backups, or the shop-floor transfer path
