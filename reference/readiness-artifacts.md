# reference/readiness-artifacts.md

> **Job this file does:** it gives the researcher practical output shapes. The
> researcher should not end with "hope that helps." It should leave the contractor
> with a safe artifact: a question list, a scope map, a readiness snapshot, or an
> evidence gap list.

---

## Artifact 1: Safe Intake Summary

Use when the conversation has enough facts to orient the user.

```text
Current Intake
- Work/customer:
- Data type:
- Confidence:
- Data locations:
- People/providers:
- Current systems:
- Claimed obligation:
- Known artifacts:
- Source claims:
- Biggest unknown:
- Next question:
```

Rules:

- Keep it short.
- Mark unknowns as unknown.
- Never include sensitive contents.
- Do not claim the file `reference/intake.md` has been updated.

## Artifact 2: CUI/FCI Clarification Questions

Use when the contractor does not know whether the work involves FCI or CUI.

```text
Questions to take to the prime or contracting officer
1. Does this contract or subcontract involve CUI?
2. If yes, which CUI category or marking applies?
3. Where is the CUI expected to be received, stored, processed, or transmitted?
4. Which DFARS/FAR clauses are included or flowed down?
5. Is CMMC Level 2 required for this work, and is the expected assessment path
   self-assessment or C3PAO certification?
6. What deadline applies to this contract or solicitation?
```

Rules:

- Present this as a question list, not a legal conclusion.
- Encourage written confirmation when practical.

## Artifact 3: Scope Map

Use when the contractor starts naming systems and workflows.

```text
Scope Map Draft
- CUI assets:
- Security protection assets:
- Contractor risk managed assets:
- Specialized assets:
- External service providers:
- Candidate out-of-scope assets:
- Scope leaks to test:
```

Common scope leaks:

- email attachments
- mobile mail clients
- local downloads
- browser sync
- unmanaged devices
- MSP admin access
- backups
- ticketing systems
- shared drives
- logs and SIEM

Rules:

- Treat the map as a hypothesis until validated.
- Ask how each boundary is enforced and evidenced.

## Artifact 4: Readiness Snapshot

Use when the user asks "where do we stand?"

```text
Readiness Snapshot
- Likely data type:
- Confidence:
- Likely CMMC level:
- Assessment path:
- Scope boundary:
- Scope risks:
- Top hard-stop risks:
- Top POA&M candidates:
- Evidence gaps:
- Source-confidence notes:
- Next three actions:
- Human/source to confirm:
```

Rules:

- Say "likely" when the answer is not binding.
- Never present the snapshot as certification.
- Include the one official source or human that can settle the biggest unknown.
- In ordinary chat, render the snapshot as Markdown bullets, not a fenced code
  block. Fenced text is only for copy/paste mode when the user asks.

## Artifact 5: Evidence Gap List

Use when the user has named tools or controls but not evidence.

```text
Evidence Gap List
- Claim:
- Evidence needed:
- Current evidence:
- Missing proof:
- Priority:
- Why it matters:
```

Examples of evidence:

- SSP section
- policy/procedure
- configuration screenshot
- exported setting
- ticket/change record
- training record
- access review record
- log sample
- incident response test
- vendor responsibility matrix

Rules:

- Do not accept tool ownership as evidence.
- Ask what an assessor would be able to inspect.

## Artifact 6: Source Weighing Note

Use when the user brings a claim from a vendor, prime, consultant, blog, or forum.

```text
Source Weighing Note
- Claim:
- Source:
- Authority tier:
- What the source can tell us:
- What it cannot decide:
- Higher-authority source to check:
- Safe next question:
```

Rules:

- Be skeptical without being hostile.
- A prime's operational demand may matter commercially, even when it is not the
  same as official rule text. If it is flowed into the subcontract, treat it as a
  contract requirement; if it is only an email summary, verify the underlying
  clause, solicitation, or contracting-officer direction.
- A vendor may be useful and still not be authoritative.

## Artifact 7: Web Demo Output Contract

Use for the future interactive web app. The app should show these fields beside
the chat so the investigative process is visible:

```text
Investigation State
- Stage:
- Data type:
- Confidence:
- Known systems:
- Active failure mode:
- Source tier in use:
- Biggest unknown:
- Next question:
```

Rules:

- The side panel must not store sensitive content.
- It should update only from safe abstractions.
- It should make the researcher's reasoning legible without turning the chat into
  a form.
