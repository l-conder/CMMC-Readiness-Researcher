# reference/common-failure-modes.md

> **Job this file does:** it gives the researcher the traps to actively hunt.
> These are the places small defense contractors lose time, money, or assessment
> credibility. A summarizer waits for the user to name them. A researcher looks
> for them.

---

## 1. Checklist-first thinking

**Pattern:** The contractor asks for "the CMMC controls" before establishing what
data they handle.

**Why it matters:** The obligation changes radically depending on whether the work
involves FCI only, CUI, or a higher-sensitivity program.

**Researcher move:** Hold the checklist. Ask what kind of government information
the contract involves, in general terms only.

## 2. CUI uncertainty treated as certainty

**Pattern:** The contractor says "I think it is CUI" or "the prime says it might
be CUI" without markings, clause context, or customer confirmation.

**Why it matters:** The researcher can reason about likelihood, but the binding
CUI determination comes from the contract and government customer.

**Researcher move:** Ask what the contract, prime, or customer has said; route the
binding question to the contracting officer or prime in writing.

## 3. CUI in email

**Pattern:** The contractor says CUI lives in SharePoint, an enclave, or a secure
drive, but drawings, specs, or attachments arrive by email first.

**Why it matters:** Email may be in scope if it stores, transmits, or exposes CUI.
Many contractors under-scope because they map the final storage location but not
the intake path.

**Researcher move:** Ask where the data arrives, whether attachments remain in
mailboxes, whether users forward it, and whether mobile mail clients can access
it.

## 4. SaaS sprawl

**Pattern:** CUI is copied into ticketing systems, CRM notes, file sync tools,
chat, support portals, design tools, or unmanaged SaaS apps.

**Why it matters:** Any service that stores, processes, or transmits CUI becomes a
scope and authorization question.

**Researcher move:** Ask "where else does this information land when work gets
done?" rather than "where is the official repository?"

## 5. MSP/ESP assumed to close the issue

**Pattern:** The contractor says "our MSP handles security" as if that removes
the contractor's responsibility.

**Why it matters:** External service providers that touch CUI systems or security
protection assets become part of the readiness picture.

**Researcher move:** Ask what the MSP can access, what they administer, whether
they touch logs/identity/endpoints/backups, and what evidence they can provide.

## 6. Inheritance misunderstood

**Pattern:** The contractor buys GCC High, a FedRAMP service, or a compliance
platform and assumes controls are done.

**Why it matters:** Inherited controls reduce work but rarely eliminate the
contractor's side of shared responsibility.

**Researcher move:** Separate provider responsibility from contractor
responsibility. Ask what is inherited, what is partially inherited, and what the
SSP says.

## 7. Scope boundary based on intention, not paths

**Pattern:** The contractor says a system is out of scope because they intend CUI
not to go there.

**Why it matters:** Assessors care about actual paths: sync, downloads, email,
identity, admin access, backups, shared credentials, and logs.

**Researcher move:** Test the boundary. Ask how separation is enforced and how the
contractor can prove it.

## 8. Rev. 3 treated as current CMMC baseline

**Pattern:** A vendor or blog says NIST SP 800-171 Rev. 3 is newest, so the
contractor must align to Rev. 3 now.

**Why it matters:** Newest publication is not automatically the version assessed
under CMMC. The contract and CMMC program determine the binding baseline.

**Researcher move:** Work the current binding obligation while flagging Rev. 3 as
future direction. Route date-sensitive claims to official source confirmation.

## 9. SPRS score treated as proof

**Pattern:** The contractor has a high SPRS score and assumes readiness.

**Why it matters:** SPRS is self-assessment. It can be wrong if the scope is wrong
or if evidence does not satisfy assessment objectives.

**Researcher move:** Ask how the score was calculated, which controls were counted
as met, and whether evidence exists for each objective.

## 10. SSP written after the environment

**Pattern:** The contractor treats the SSP as paperwork to fill out after tools
are deployed.

**Why it matters:** The SSP defines the boundary and the story the assessor will
test. A vague SSP can sink a technically decent environment.

**Researcher move:** Ask what the SSP currently says about boundary, inheritance,
and implementation. If no SSP exists, make it an early artifact.

## 11. POA&M used for hard stops

**Pattern:** The contractor assumes any gap can be put on a POA&M.

**Why it matters:** Some gaps cannot be deferred at assessment time, and POA&M
eligibility rules are date- and rule-sensitive.

**Researcher move:** Split gaps into hard-stop, likely POA&M-eligible, and
uncertain. Confirm current thresholds against official CMMC sources.

## 12. Evidence confused with implementation

**Pattern:** The contractor says "we have MFA" or "we log events" but cannot show
policy, configuration, screenshots, logs, tickets, training records, or review
cadence.

**Why it matters:** CMMC is assessed through evidence. A control that exists but
cannot be demonstrated may still fail.

**Researcher move:** Ask "what evidence would prove that to an assessor?" and map
implementation claims to artifacts.

## 13. COTS off-ramp missed

**Pattern:** A pure commercial off-the-shelf reseller is told by a prime to pursue
Level 2 without checking whether CUI is actually handled.

**Why it matters:** Some businesses may have a much narrower obligation than the
prime's blanket message suggests.

**Researcher move:** Investigate what the subcontract actually requires, whether
the contractor receives or creates CUI, and what the prime/contracting officer
will confirm.

## 14. AI tool misuse

**Pattern:** The contractor wants to upload contracts, drawings, or technical
specifications to an AI tool for classification or summarization.

**Why it matters:** That may create a data spillage if the tool is not authorized
for controlled information.

**Researcher move:** Stop the content flow. Ask for category, location, workflow,
and markings instead of contents.

## How To Use This File

When a user describes their environment, silently scan for these failure modes.
If one appears, name it plainly and ask the next question that would prove or
disprove it.

Do not list all failure modes to the user. Surface the one that matters now.
