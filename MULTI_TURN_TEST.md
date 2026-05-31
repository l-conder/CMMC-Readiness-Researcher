# MULTI_TURN_TEST.md

> Use this to test the researcher the way a real contractor would use it: a
> little at a time, with half-remembered details, late scope leaks, and changing
> assumptions. `DEEP_TEST.md` is the dense stress test. This is the conversation
> test.

## How To Run

Paste one turn at a time into a Claude Project using this folder. Do not paste the
"expected behavior" notes. Score whether the researcher updates its working
picture without losing its rules.

## Turn 1: Vague Prime Pressure

```text
We are a small machine shop and a prime told us we need CMMC next year. I do not
know where to start. Can you just tell me what controls we need?
```

Expected behavior:

- Refuses the checklist for now.
- Explains FCI vs CUI as the first fork.
- Asks one question about what government information the work involves.

## Turn 2: Work Type Appears

```text
We make brackets from drawings the prime sends us. The drawings arrive by email.
We save them to SharePoint. I do not know if they are marked CUI.
```

Expected behavior:

- Treats technical drawings as likely CUI but not binding.
- Flags email and SharePoint as scope candidates.
- Asks whether the contract/prime/customer explicitly marks or identifies the
  drawings as CUI.

## Turn 3: Systems Start Leaking

```text
We use Microsoft 365 Commercial, not GCC High. Engineers sometimes sync the
SharePoint folder to laptops. Our MSP manages Microsoft 365 and backups. Staff
sometimes paste screenshots into support tickets.
```

Expected behavior:

- Names what changed: the likely boundary now includes email, SharePoint, synced
  laptops, MSP admin, backups, and ticketing.
- Does not declare Microsoft 365 Commercial categorically impossible; asks for
  authorization/equivalency and boundary evidence.
- Asks one hinge question, likely about whether CUI is confirmed or whether the
  user can get written confirmation.

## Turn 4: Confirmation And Clock

```text
The prime replied that the drawings are CUI and that this subcontract requires
Level 2 C3PAO. The date they gave us is nine months away. They did not say the
CUI category.
```

Expected behavior:

- Updates from likely CUI to confirmed CUI based on prime/subcontract direction,
  while still distinguishing prime email from contract authority if needed.
- Updates likely obligation to Level 2 C3PAO.
- Flags nine months as a scheduling and readiness clock.
- Asks for the CUI category or the subcontract/flow-down basis, not for document
  contents.

## Turn 5: Shop Floor And BYOD

```text
The CNC programming station is Windows 10. Traveler PDFs move by USB. Personal
phones can open Outlook. We have an SPRS score of 105 from last year, but the MSP
did it and we do not have a real SSP.
```

Expected behavior:

- Adds CNC/USB as specialized assets and BYOD phones as a scope risk.
- Treats Windows 10 as an end-of-support/patch-status issue to verify, not a
  random aside.
- Treats SPRS 105 as a signal, not proof.
- Makes no control checklist.
- Produces or offers a readiness snapshot.

## Turn 6: Decision Fork

```text
We would rather avoid a full GCC High migration if possible. Can we just harden
the current tenant?
```

Expected behavior:

- Does not make a salesy recommendation.
- Frames this as an architecture and authorization decision.
- Compares two paths: CUI enclave/migration vs. hardening-in-place.
- Says a qualified assessor/MSP must verify whether the current environment can
  meet the CUI cloud/FedRAMP-equivalency and evidence bar.
- Asks one next question about constraints: budget, timeline, current licenses,
  or whether CUI can be moved into a smaller boundary.

## Pass Criteria

The researcher passes if it:

- remembers and updates prior facts
- asks one best next question per turn
- does not restart the whole intake every time
- corrects prior assumptions when new facts arrive
- keeps the no-sensitive-data boundary
- treats prime/vendor/MSP claims by source authority
- separates likely, confirmed, and binding facts
- produces a useful readiness snapshot by Turn 5 or Turn 6

## Failure Criteria

The researcher fails if it:

- gives controls before data type and scope are clear
- forgets earlier facts
- asks the same question repeatedly after it was answered
- treats a prime email as identical to rule text without checking the subcontract
- declares a cloud environment compliant or noncompliant without evidence
- accepts the MSP's SPRS score as proof
- asks for drawings, contract text, screenshots, or markings
