# reference/source-list.md

> **Job this file does:** it gives the researcher concrete, official places to
> send the user when a claim needs confirmation. `source-authority.md` explains how
> to rank sources; this file names the sources that usually settle the question.
> Use these links as routing targets, not as a substitute for checking the current
> publication when the answer affects a real contract, deadline, or attestation.

---

## Primary CMMC and contract sources

**DoD CMMC program site**  
https://dodcio.defense.gov/CMMC/

Use for program-level CMMC updates, implementation notices, model materials, and
official DoD framing. This is the first stop for "what is the current CMMC
program posture?"

**CMMC Program rule, 32 CFR Part 170**  
https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-M/part-170

Use for the current codified CMMC program rule. When a blog, vendor, or prime says
"CMMC requires X," this is one of the highest-authority places to verify the
program requirement.

**CMMC final rule as published in the Federal Register**  
https://www.federalregister.gov/documents/2024/10/15/2024-22905/cybersecurity-maturity-model-certification-cmmc-program

Use for the rule's original publication history, effective date, definitions, and
DoD commentary. Prefer the eCFR link for the current codified text.

**DFARS CMMC acquisition rule, 48 CFR Part 204.75**  
https://www.ecfr.gov/current/title-48/chapter-2/subchapter-D/part-204/subpart-204.75

Use for how CMMC requirements enter solicitations and contracts. This is critical
when the question is not "what is CMMC?" but "when does it appear in a contract?"

**DFARS 252.204-7021**  
https://www.acquisition.gov/dfars/252.204-7021-cybersecurity-maturity-model-certification-requirements.

Use for the CMMC contract clause itself. If the user is asking whether a contract
requires CMMC, the clause language and the contracting officer matter more than
general commentary.

**DFARS 252.204-7012**  
https://www.acquisition.gov/dfars/252.204-7012-safeguarding-covered-defense-information-and-cyber-incident-reporting.

Use for safeguarding covered defense information and cyber incident reporting.
This is one of the key contractual hooks for CUI handling in defense contracts.

**DFARS 252.204-7019 and 252.204-7020**  
https://www.acquisition.gov/dfars/252.204-7019-notice-nist-sp-800-171-dod-assessment-requirements.  
https://www.acquisition.gov/dfars/252.204-7020-nist-sp-800-171-dod-assessment-requirements.

Use for SPRS and DoD assessment requirement questions. These clauses often matter
before a formal CMMC certification requirement appears.

**FAR 52.204-21**  
https://www.acquisition.gov/far/52.204-21

Use for the 15 basic safeguarding requirements tied to Federal Contract
Information. This is the Level 1 / FCI baseline source.

---

## NIST standards and assessment material

**NIST SP 800-171 Rev. 2**  
https://csrc.nist.gov/pubs/sp/800/171/r2/final

Use for the 110-requirement baseline CMMC Level 2 is currently built around. If
the user asks "what control text applies to me today," this is usually the working
standard, subject to their contract and assessment path.

**NIST SP 800-171A Rev. 2**  
https://csrc.nist.gov/pubs/sp/800/171/a/r2/final

Use for assessment objectives tied to SP 800-171 Rev. 2. This is where "we meet
the control" turns into "can we demonstrate every objective?"

**NIST SP 800-171 Rev. 3**  
https://csrc.nist.gov/pubs/sp/800/171/r3/final

Use for the direction of travel and future planning. Do not treat Rev. 3 as the
current CMMC assessment baseline unless the contract or official CMMC material
says so.

**NIST SP 800-172**  
https://csrc.nist.gov/pubs/sp/800/172/final

Use for enhanced requirements relevant to the highest-sensitivity cases and CMMC
Level 3 conversations.

---

## CUI, cloud, and assessor ecosystem sources

**NARA CUI Registry**  
https://www.archives.gov/cui

Use for CUI categories, markings, and official CUI program context. The registry
helps frame the question, but the binding CUI determination still comes from the
contract and government customer.

**FedRAMP Marketplace**  
https://marketplace.fedramp.gov/

Use when a cloud or SaaS provider touches CUI and the user needs to verify whether
the service has a relevant FedRAMP authorization. Product claims should be checked
against the marketplace and the provider's authorization boundary.

**The Cyber AB Marketplace**  
https://cyberab.org/Catalog

Use to verify C3PAOs, Registered Provider Organizations, Registered Practitioners,
and other official CMMC ecosystem roles. This is the place to separate "consultant
who can help" from "assessor who can certify."

---

## How to route users to these sources

Do not dump this list on a user by default. Name the one source that settles the
current question, explain why it has authority, and say what to look for there.

Examples:

- "That sounds like a contract-clause question, so the source to check is DFARS
  252.204-7021 and the contracting officer's direction."
- "For the control text itself, use NIST SP 800-171 Rev. 2; the vendor's checklist
  is secondary."
- "For whether that SaaS service can hold CUI, check the FedRAMP Marketplace and
  the provider's authorization boundary, not just the sales page."
