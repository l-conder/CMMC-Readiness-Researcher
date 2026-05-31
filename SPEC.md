# SPEC.md

## §G

G1. Build a demo web app that proves the CMMC Readiness Researcher works as an investigative, source-aware, no-sensitive-data readiness partner over the folder knowledge.

## §C

C1. Folder remains canonical; app is surface, not new brain.
C2. App must not invite uploads or pasted controlled content.
C3. App must warn against CUI, FCI, contract text, drawings, specs, and sensitive attachments before chat starts.
C4. App must support safe demo scenarios so judges can test without real data.
C5. App must show investigation state beside chat: stage, data type, confidence, systems, active risk, source tier, biggest unknown, next question.
C6. App must demonstrate one-question-at-a-time behavior.
C7. App must demonstrate source ranking with official source links.
C8. App must end useful flows with a Readiness Snapshot, not a generic summary.
C9. App must keep copy plain, calm, specific, and not fear-based.
C10. App must work without signup for judging.
C11. App must be portfolio-polished: README path, demo path, screenshots or video plan.
C12. App must not claim certification, legal advice, or authoritative CUI classification.
C13. App should be deployable to Vercel, Netlify, Cloudflare Workers, or similar static/serverless host.
C14. If no backend/API key is configured, app should still run in deterministic demo mode.
C15. Any model integration must use the existing researcher files as prompt/context source.

## §I

I.web. Browser UI for public demo and judging.
I.chat. Chat surface that sends user messages to either demo engine or model backend.
I.state. Visible investigation state panel.
I.sources. Source drawer linking official CMMC/NIST/FAR/DFARS/NARA/FedRAMP/Cyber AB sources.
I.scenarios. Preloaded safe demo prompts, including quick examples and DEEP_TEST.
I.export. Copy/download safe Readiness Snapshot.
I.env. Optional API key/model config kept out of repo.
I.docs. README/JUDGE_GUIDE/SPEC describe install, run, test, and demo path.
I.demo. Static deterministic demo lives at docs/index.html.

## §V

V1. No sensitive-data intake: UI, prompts, and model instructions refuse CUI/FCI/contract/spec content and redirect to category/location/workflow.
V2. Folder-canonical: app prompt/context loads from markdown files or generated bundle derived from them; duplicated app copy cannot become the source of truth.
V3. First-turn behavior: broad CMMC/control requests do not receive a checklist; app asks the FCI/CUI fork first.
V4. One-question discipline: normal investigative turns ask one primary decision-relevant question and explain why it matters.
V5. Source hierarchy visible: when a source claim matters, response names source tier and points to higher-authority source.
V6. Uncertainty honesty: app labels likely vs binding determinations and routes contract/CUI/legal/certification questions to the right human/source.
V7. Scope reasoning visible: state panel tracks systems, people/providers, scope risks, and active failure mode from safe abstractions only.
V8. Demo-ready without secrets: safe canned scenarios run locally without API keys.
V9. Snapshot contract: closing output includes data type, confidence, likely level/path, scope boundary, top risks, evidence gaps, next actions, and confirmation source.
V10. No fake persistence: app must not imply project markdown or intake files are being rewritten during chat.
V11. Accessibility baseline: keyboard usable, readable contrast, responsive desktop/mobile layout, no text overlap.
V12. Security baseline: no sensitive chat storage by default; no analytics capturing message contents unless explicitly disabled or documented.
V13. Judge path: a stranger can open README, run demo, test adversarial prompts, and understand what behavior passes.

## §T

id|status|task|cites
T1|x|Choose stack and repo shape for web demo|C13,C14,V8,V11
T2|x|Create app shell with chat, state panel, source drawer, and scenario rail|I.web,I.chat,I.state,I.sources,I.scenarios,V7,V11
T3|x|Add pre-chat safety gate and persistent no-sensitive-data banner|C2,C3,V1,V12
T4|x|Build deterministic demo engine for safe scenarios|C4,C14,I.scenarios,V3,V4,V5,V6,V8,V9
T5|.|Create prompt/context bundle from researcher markdown files|C1,C15,V2
T6|.|Add optional model backend adapter with env config|I.chat,I.env,C15,V1,V2,V12
T7|x|Implement investigation state extraction from safe abstractions|I.state,V7,V10
T8|x|Implement Readiness Snapshot copy/download|I.export,V9,V12
T9|x|Add source drawer using reference/source-list.md|I.sources,C7,V5
T10|.|Add adversarial test fixtures from JUDGE_GUIDE.md|I.docs,V1,V3,V4,V5,V6,V13
T11|x|Write web app README section: run, deploy, demo, safety limits|I.docs,C10,C11,C12,V13
T12|.|Create screenshots or short demo-video script|C11,V13
T13|.|Run local manual QA on desktop and mobile viewports|V11,V13
T14|.|Run full judge prompt suite and record pass/fail notes|V1,V3,V4,V5,V6,V7,V9,V13
T15|x|Add DEEP_TEST scenario to static demo|I.demo,I.scenarios,V7,V9,V13

## §B

id|date|cause|fix
