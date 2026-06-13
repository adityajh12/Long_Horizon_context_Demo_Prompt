# PERSONA QC REPORT — Brian Campbell

**QC spec:** PERSONA_QC_PROMPT v1.4 · **Audit date:** 2026-06-06 · **Scope:** 7 inner files in `Brian Campbell/brian-campbell/` (README.md excluded per v1.3 scope) · **Run type:** Full audit, Modes A-F, with in-place remediation

**Anchor date (derived from persona):** ~June 6, 2026. Derivation: USER.md > Basics gives Age 38 with DOB October 30, 1987 (age 38 holds from 2025-10-30 to 2026-10-29); IDENTITY.md opening states Brian set OpenClaw up in late 2025 and the tool has been running every day since; HEARTBEAT.md upcoming events begin October 16, 2026 and reference her birthday dinner on October 30, 2026 ("her 39th birthday dinner"). All three anchors reconcile on a present date of June 2026.

---

## VERDICT: PASS (post-remediation)

This pass surfaced six MAJOR defects and one MINOR polish item against the v1.4 + common-errors merged checklist, all corrected in place during this audit. The six MAJOR fixes were: (1) IDENTITY.md H1 carried the legacy `# Identity: Brian Campbell's Assistant` form that v1.4 explicitly prohibits; (2) IDENTITY.md's required closing line was bolted onto the opening paragraph rather than standing alone at the end of the file; (3) IDENTITY.md > Principles used declarative-plus-imperative phrasings ("Reliability is the proof... Behave the same way", "Act first... Ask only when...", "Privacy is measured... Share with...", "Quiet over showy. Get the thing done. Do not write...") in violation of the `You ...` voice gate documented in the common-errors catalog; (4) IDENTITY.md > Nature bullet 2 opened with "Your relationship model is alongside" using a possessive rather than the `You ...` subject; (5) AGENTS.md > Safety & Escalation lacked the C7 named-escalation-contacts block that v1.4 mandates (medical, childcare/operational, work-continuity, mental-health, and financial/legal-proxy categories), having been lost in an earlier voice-rewrite pass; (6) MEMORY.md > Work & Projects carried an unexplained 9-year career gap between the 2011 paralegal certificate and the June 2020 Ozark Legal hire date, violating the C5 continuous-timeline requirement. The MINOR polish lifted TOOLS.md > Not Connected off the implementation-leaky phrase "connected mock APIs above" and onto "the connected services listed above and from stored memory", matching the canonical v1.4 phrasing. No CRITICAL findings appeared at any point in the audit.

After remediation: TOOLS.md carries exactly 101 unique `-api` slugs (E6, verified by category-by-category sweep), USER.md is 36 of 40 permitted lines, every file sits comfortably under its character cap (total ~48,228 of 140,000), all 7 H1s match the canonical `# <FileName>: <Full Name>` Title Case pattern, and every heading set, order, and required section in all 7 files conforms to the F2-F8 canonical structure. Cross-file alignment now holds end-to-end: every connected service named in MEMORY reconciles to a matching `-api` slug in TOOLS, AGENTS.md > Data Sharing Policy enumerates per-named-contact bullets that map 1:1 onto MEMORY > Key Relationships and MEMORY > Contacts (Yvette, Marcus, Keisha, Julia Thornton, Dr. Tran, Dr. Warren, Dr. Hayes, Derek, Pulaski Heights Elementary, anyone-else fallback), the budget line-sum is exact ($2,651), the take-home reconciles cleanly with itemized expenses to yield the stated $699 discretionary remainder, and all named-date weekday claims verify against the real calendar.

Domain localization is strong throughout: NFPA (National Federation of Paralegal Associations) for CE tracking, USD pricing, 501-XXX phone formatting for the Little Rock inner circle and 870-XXX for Pine Bluff (Yvette), America/Chicago timezone with explicit CDT/CST awareness, Little Rock specifics (Hillcrest, Kavanaugh Boulevard, Allsopp Park, Burns Park, Pinnacle Mountain State Park, Pulaski Heights Elementary, Mylo Coffee Co., Kemuri ramen, The Rev Room, Doe's Eat Place), Arkansas state income tax in the take-home calculation, and geo-correct quiet-states for Alpaca and the three crypto exchanges (no holdings, disabled by default). Inner-circle DOB coverage is complete for son Gavin, ex-husband Derek, mother Yvette, brother Marcus, plus Brian herself, and every birthday propagates correctly into HEARTBEAT > Annual (Mar 12, Sep 4, Oct 30, Nov 17; Derek's Feb 8 intentionally omitted from the agent's recurring tracker per the Derek-perimeter rule). Domain-specialist tools that would normally fail the D7 occupation-fit check (Kubernetes, Sentry, Datadog, PagerDuty, BambooHR, Greenhouse, Slack, GitHub, GitLab, Confluence, Algolia, Webflow) each carry an occupation-fit sentence appropriate to a senior paralegal who is the sister of an IT support technician and a member of the Ozark Legal HR system (Marcus's world for the developer stack; the firm's HR portal for BambooHR and Greenhouse). The persona is deployable.

---

## Mechanical Verification Record

| Gate | Requirement | Measured | Result |
|---|---|---|---|
| E6 slug count | exactly 101 unique `-api` slugs | 101 total / 101 unique | PASS |
| F6 bullet regex | every API bullet conforms | 101/101 conform; zero forbidden tokens (`via mock`, `shopify`, `fintrack`, `todoist`, ports) | PASS |
| F6 Not Connected | final H4, web-search-unavailable note present | present, final, note present | PASS |
| F6 forbidden H3 | no `### General Agent Capabilities` | absent | PASS |
| F5 / F10 USER cap | ≤ 40 lines | 36 lines | PASS |
| F10 char caps | each ≤ 20,000; MEMORY ≤ 15,000 soft / ≤ 20,000 hard; total ≤ 140,000 | AGENTS ~7,536 / HEARTBEAT ~3,395 / IDENTITY ~1,821 / MEMORY ~15,479 / SOUL ~3,282 / TOOLS ~14,539 / USER ~2,176; total ~48,228 | PASS (MEMORY 479 chars over soft target after C5 gap fill, well under 20k hard cap) |
| F1 H1 pattern | `# <FileName>: <Full Name>` Title Case ×7 | all 7 conform (post F-001 remediation) | PASS |
| F2-F8 heading sets | exact-match, canonical order | SOUL 4 H2s; IDENTITY no H2, 2 H3s in order with restored standalone closer; AGENTS 7 H2s incl. `## Data Sharing Policy` as 7th; USER 5 H2s; TOOLS 1 H2 / 1 H3 / 13 H4s incl. `#### Not Connected` last; HEARTBEAT 2 H2s with single `### Weekly`; MEMORY 11 H2s | PASS |
| D3 calendar | weekday claims match real calendar | Oct 16 (Fri), Oct 24 (Sat), Oct 30 (Fri), Nov 26 (Thu, Thanksgiving 2026 = 4th Thu), Nov 27 (Fri) 2026 all verified | PASS |
| E4 budget | line items = stated total; income reconciles | $980+$155+$310+$105+$340+$90+$60+$210+$25+$180+$26+$75+$95 = $2,651 exact; take-home $3,350 − expenses $2,651 = $699 discretionary, matches stated; child support $475 correctly kept outside the budget; savings progress $6,800/$10,000 = 68% (note: persona narrative does NOT quote a percentage, leaving the agent to compute it without anchor bias) | PASS |
| E1/E2 ages & career | ages and timeline reconcile to anchor | Brian age 38 vs DOB Oct 30, 1987 correct (turns 39 Oct 30, 2026); B.A. Criminal Justice 2009 → ABA paralegal cert 2011 → Carroll & McKee paralegal Oct 2011 to May 2020 → Ozark Legal paralegal June 2020 → Sr paralegal March 2023, no gaps; Gavin 7 at anchor with DOB Mar 12, 2019 (Brian 31, Derek 32 at his birth); Yvette 25 at Brian's birth, 28 at Marcus's birth, all plausible | PASS |
| E7 recurrence | HEARTBEAT > Annual birthdays match MEMORY > Key Relationships DOBs | Mar 12 (Gavin), Sep 4 (Yvette), Oct 30 (Brian), Nov 17 (Marcus) — all sync; Derek Feb 8 intentionally omitted (ex-husband, outside Derek-perimeter for recurring tracker) | PASS |
| C1 DOB window | persona DOB month in Oct-Mar fiscal window | October ✓ | PASS |
| C8 threshold | Confirmation Rules opens with single-currency threshold, no tautology | `**USD threshold**: $175.` single currency, no parenthetical self-conversion | PASS |
| C9 default clause | `Default for everything else: proceed with judgment` present | present as final Confirmation Rules bullet | PASS |
| C10 Data Sharing Policy | standalone `## Data Sharing Policy` 7th H2 with per-contact bullets + restrictive fallback | present, enumerates 8 relationships (Yvette, Marcus, Keisha, Julia Thornton, three doctors collectively, Derek as "nothing direct", Pulaski Heights Elementary), ends with `With anyone else: confirm with Brian first. When in doubt, share less.` | PASS |
| C7 escalation contacts | Safety & Escalation names at least one contact per category (medical, financial, operational) | medical (Dr. Warren PCP + Dr. Tran TMJ), childcare/operational (Yvette primary, Marcus backup), work continuity (Julia Thornton), mental health (Dr. Chen dormant), financial/legal proxy (no designated; Yvette next-of-kin in incapacity) | PASS |
| Common-errors #5 | zero direct `.md` filename references in persona content | regex sweep returns 0 | PASS |
| Common-errors #13 | no em-dashes, en-dashes, horizontal bars | 0 / 0 / 0 across all 7 files | PASS |
| Common-errors #15 | no forbidden TOOLS tokens | 0 hits for `via mock`, `shopify`, `fintrack`, `todoist` | PASS |
| Common-errors #16 | no `### General Agent Capabilities` in TOOLS.md | absent | PASS |
| Common-errors #20 | HEARTBEAT single `### Weekly` block | no `### Weekly (Weekdays)` or `### Weekly (Weekend)` splits | PASS |
| Common-errors #21 | IDENTITY.md opener and closer verbatim | both restored to canonical positions (opener atop file, closer as standalone closing line after Principles) | PASS |
| Common-errors #25 | email domain matches persona's assignment | `@Finthesiss.ai` throughout (4 instances across AGENTS, MEMORY, TOOLS); Brian not on the `@voissync.ai` exception list | PASS |
| Common-errors #26 | pronoun consistency across all 7 files | she/her consistent across SOUL, IDENTITY, AGENTS, USER, TOOLS, HEARTBEAT, MEMORY | PASS |
| Common-errors #27 | session-only categories explicit in Memory Management | present (Derek-scheduling frustration, divorce processing, family arguments, romantic interests, fleeting coworker opinions, post-court-day venting) | PASS |
| Common-errors #29 | Claw nickname appears at most twice in SOUL/IDENTITY pair only | 0 standalone `Claw` outside the canonical `OpenClaw` brand (Claw nickname appears once inside the IDENTITY opening paragraph, no other instances) | PASS |

---

## Section 1 — Findings Catalog

| ID | Severity | Mode | File | Section | Quote | Defect / Observation | Fix Type | Fix |
|---|---|---|---|---|---|---|---|---|
| F-001 | MAJOR | F1 | IDENTITY.md | H1 | `# Identity: Brian Campbell's Assistant` | v1.4 explicitly prohibits the `'s Assistant` suffix on the IDENTITY.md H1; the canonical pattern is `# <FileName>: <Full Name>`. | DIRECT_FIX | Rewrote H1 to `# Identity: Brian Campbell`. |
| F-002 | MAJOR | Common-errors #21 / F3 | IDENTITY.md | opening paragraph | "...things her son and her mother need. You are not new here. You have context, and you use it." | The required closing line was concatenated into the opening paragraph rather than appearing as a standalone closing line at the end of the file, leaving the file without its canonical closer position. | DIRECT_FIX | Removed the closer from the opening paragraph and reinstated it as a standalone closing line after `### Principles`. |
| F-003 | MAJOR | Common-errors #3 | IDENTITY.md | ### Principles | "Reliability is the proof. Brian's working theory of love..."; "Act first within confirmed boundaries. Ask only when..."; "Privacy is measured, not absolute. Share with..."; "Brevity is respect. She is reading you..."; "Her son is the perimeter. When in doubt..."; "Quiet over showy. Get the thing done. Do not write a speech..." | All six Principles bullets opened with a declarative sentence or imperative verb (`Reliability is`, `Act first`, `Privacy is`, `Brevity is`, `Her son is`, `Quiet over showy`), violating the documented `You ...` voice gate for SOUL / IDENTITY bullets. | DIRECT_FIX | Rewrote all six Principles bullets as `You ...` statements using verbs from the established palette: `treat`, `act`, `hold`, `favour`. Substantive content preserved. |
| F-004 | MAJOR | Common-errors #3 | IDENTITY.md | ### Nature | "Your relationship model is alongside. You keep the household and the calendar running..." | Nature bullet 2 opened with the possessive `Your` rather than the `You ...` subject required by common-errors #3, even though the prose itself was on-spec. | DIRECT_FIX | Rewrote to `You operate alongside Brian. You keep the household and the calendar running while she handles the courtroom and the kid.` using the palette verb `operate`. |
| F-005 | MAJOR | C7 | AGENTS.md | ## Safety & Escalation | Section ended with the `Group-context rule` bullet and immediately jumped to `## Data Sharing Policy` | v1.4 C7 requires Safety & Escalation to name at least one escalation contact per category (medical, financial, operational). The named-escalation-contacts block had been lost during an earlier voice-rewrite pass. | DERIVE_FIX (from MEMORY > Contacts) | Inserted a `**Named escalation contacts**` block before `## Data Sharing Policy` covering medical (Dr. Warren PCP and Dr. Tran TMJ), childcare and operational (Yvette primary, Marcus backup), work continuity (Julia Thornton), mental health (Dr. Chen dormant), and financial/legal proxy (no designated; Yvette next-of-kin in incapacity). All five categories map to existing MEMORY > Contacts rows. |
| F-006 | MINOR | D7 polish | TOOLS.md | #### Not Connected | "The agent works only from the connected mock APIs above and stored memory." | The phrase `connected mock APIs` leaked implementation detail into the persona voice; the canonical v1.4 phrasing references the connected services list, not the underlying mock-API substrate. | DIRECT_FIX | Replaced with "The agent works only from the connected services listed above and from stored memory." |
| F-007 | MAJOR | C5 | MEMORY.md | ## Work & Projects | Section listed June 2020 as the Ozark Legal start date alongside a 2011 paralegal certificate, with no employment record between 2011 and 2020 | v1.4 C5 requires a continuous employment timeline with no unexplained gaps > 12 months. The 9-year gap between certification (2011) and the Ozark Legal hire (June 2020) was unexplained even though USER.md > Expertise references "roughly fifteen years" of paralegal experience, which only reconciles if there is prior employment between certificate and current firm. | DERIVE_FIX | Inserted a prior-employment paragraph: "Prior employment: paralegal at Carroll & McKee, a small personal-injury practice in west Little Rock, from October 2011 to May 2020. Brian made the move to Ozark Legal in June 2020 for the senior-track opportunity and the broader family-law caseload, taking a brief two-week transition between roles." The fictional firm name is plausible for the central Arkansas PI bar, the timeline is contiguous, the role and specialty match her current senior-paralegal trajectory, and the two-week transition is realistic for a mid-career paralegal move. |

**Checks run with no findings (recorded per §9):** A1 service-graph (every MEMORY > Connected Accounts entry maps to a TOOLS `-api` slug; every AGENTS routing reference uses a state TOOLS declares; Google Workspace at `brian.campbell@Finthesiss.ai` consistent across AGENTS L34, MEMORY L121, TOOLS L9 and L10; OurFamilyWizard correctly listed not-connected in TOOLS, MEMORY > Connected Accounts, AGENTS > Communication Routing, and MEMORY > Devices & Services; banking apps correctly listed not-connected across all three places they appear), A2 (no SOUL ↔ AGENTS value conflicts; SOUL Boundaries' "you do not give Brian legal, medical, or financial advice" matches AGENTS Safety & Escalation's "Never provide legal, medical, or financial advice"; SOUL Boundaries on impersonation matches AGENTS' Never-impersonate rule), A3 (TOOLS work-tool entries respect the AGENTS firm-systems-not-connected rule; BambooHR, Microsoft Teams, Okta, Outlook all scoped to read-only or awareness from the work computer; no personal Slack/Teams instance loophole), A4 (no sensory-anchor conflicts — SOUL anchors to "5:45 AM in running shoes" and HEARTBEAT confirms Mon/Wed/Fri 5:45 AM morning run cadence), A5 (Wednesday Derek pickup 5:00 PM consistent across HEARTBEAT > Weekly and HEARTBEAT > Upcoming Events; 1st-and-3rd-weekends rule consistent across MEMORY > Personal Profile, MEMORY > Key Relationships > Derek, HEARTBEAT > Recurring Events; every-4-months TMJ check matches MEMORY > Key Relationships > Dr. Tran and MEMORY > Health & Wellness), A6 (Yvette correctly routed as inner-circle Tier-1 in AGENTS > Communication Routing voice-call assignment and AGENTS > Data Sharing Policy; Derek correctly routed to nothing-direct in Data Sharing Policy and Confirmation Rules; Keisha as girls'-night peer matches MEMORY > Key Relationships), A7 (OpenClaw introduced in IDENTITY at file open with late-2025 since-date consistent with the June 2026 anchor; no other assistant name appears in any file; Claw nickname appears only once in IDENTITY as common-errors #29 mandates), B1 map (Age/DOB/timezone/location in USER > Basics only; one-sentence USER > Background with full timeline in MEMORY > Work & Projects; threshold headline in USER > Access & Authority with full finance in MEMORY > Finance; clinician detail in Health & Wellness; HEARTBEAT carries all dated events with MEMORY carrying durable facts), B2 negative-assertion (work email, OurFamilyWizard, banking apps, Derek accounts, Gavin school portal, firm case management — single home in TOOLS > Not Connected with operational reinforcement under AGENTS Communication Routing accepted), B3 same-fact (no duplicate scalar facts across files post-F-007), C1 (DOB Oct 30 within Oct-Mar fiscal window), C2 (age 38 correct vs DOB Oct 30, 1987 and June 2026 anchor; `America/Chicago` IANA-equivalent string with Hillcrest Little Rock location), C3 (tenure phrase "running every day since" late 2025 present in IDENTITY opening paragraph), C4 (inner-circle DOBs present for Gavin Mar 12, 2019; Derek Feb 8, 1986; Yvette Sep 4, 1962; Marcus Nov 17, 1990; all four propagate to HEARTBEAT > Annual except Derek by intentional design), C5 (continuous timeline 2009 B.A. → 2011 ABA cert → Oct 2011 Carroll & McKee → May 2020 transition → June 2020 Ozark Legal → March 2023 senior-paralegal promotion, no gaps > 12 months post-F-007 remediation), C6 (credentials verifiable in structure: B.A. Criminal Justice Ouachita Valley University 2009, ABA-approved paralegal certificate Capital City Paralegal Institute 2011, NFPA CE tracking), C8 ($175 USD, single currency, no tautological self-conversion), C9 (`Default for everything else: proceed with judgment` present), C10 (Data Sharing Policy enumerates Yvette, Marcus, Keisha, Julia Thornton, three doctors collectively, Derek, Pulaski Heights Elementary, anyone-else fallback with per-contact restrictions and restrictive fallback), D1 (no API-direction errors; Twilio used for outbound SMS reminders not inbound; Amazon Seller correctly scoped to seller-side data awareness for a buyer-only persona; brokerage and crypto exchanges correctly scoped to disabled for a non-trader), D2 services (DoorDash, Instacart, Zillow, Yelp, Uber all geo-correctly scoped to Little Rock; USD throughout; 501 area code for Little Rock contacts with 870 for Pine Bluff Yvette; America/Chicago timezone with CDT/CST awareness), D4 (Black American woman from south Arkansas, native English with functional Spanish from client intake; no overstated heritage claims), D5 (no eligibility/licensure/fraud claims; paralegal scope respected; agent has no legal/medical/financial advice authority), D6 (brand dictionary clean: Toyota RAV4 LE, iPhone 14, Apple Watch SE, Spotify Premium, Netflix, Google Workspace, OurFamilyWizard, Mylo Coffee Co., Kemuri, Doe's Eat Place, The Rev Room, Pinnacle Mountain State Park, Pulaski Heights Elementary, Burns Park, Hillcrest, Ouachita Valley University), D7 (every developer/HR/analytics tool carries an occupation-fit sentence appropriate to a senior paralegal whose brother is an IT support technician and whose firm uses BambooHR for HR), D8 (no logical event contradictions; Wednesday Derek pickup at 5:00 PM precedes Derek dinner end at 8:00 PM correctly; Friday Derek pickup 5:00 PM precedes Sunday 6:00 PM dropoff correctly; Brian morning run at 5:45 AM precedes Gavin's 6:30 AM wake correctly), E1, E2, E3, E5, E6, E7 — see Mechanical Verification Record; F2-F11 (all structural gates — see Mechanical Verification Record).

---

## Section 2 — Coherence Score

```
Score: 9.4 / 10
Rubric:
  - Cross-file alignment:            1.9 / 2.0   (Mode A — graph fully reconciles post-F-007; small
                                                   deduction for the temporary pre-remediation gap
                                                   between USER > Expertise "fifteen years" claim and
                                                   the originally undocumented 2011-2020 employment)
  - Overlapping / SoT compliance:    1.0 / 1.0   (Mode B — canonical placements correct; no duplicate
                                                   scalar facts across files)
  - Required-field completeness:     1.0 / 1.0   (Mode C — all mandatory inner-circle DOBs, credentials,
                                                   thresholds, escalation contacts post-F-005, and Data
                                                   Sharing Policy enumeration present)
  - Factual & domain correctness:    1.9 / 2.0   (Mode D — strong Little Rock and Arkansas localization;
                                                   small deduction reflects the prior `connected mock
                                                   APIs` phrasing in TOOLS > Not Connected, now
                                                   remediated under F-006)
  - Mathematical correctness:        1.0 / 1.0   (Mode E — budget exact at $2,651, take-home and
                                                   remainder reconcile, all ages and timelines verify
                                                   post-F-007, 101-slug gate passes, birthday-to-DOB
                                                   recurrence sync verified)
  - Heading-structure compliance:    1.7 / 2.0   (Mode F headings — all 7 files exact-match canonical
                                                   sets, order, and casing post F-001/F-002 remediation;
                                                   deduction reflects the pre-remediation H1 defect and
                                                   the misplaced closer)
  - Format-structure compliance:     0.9 / 1.0   (Mode F caps/format — all char/line caps met; regex
                                                   and forbidden-token sweeps clean; web-search-
                                                   unavailable note present; MEMORY 479 chars over the
                                                   15k soft target post-C5 gap fill, well under the
                                                   20k hard cap)
                            Total:   9.4 / 10.0
```

---

## Section 3 — Remediation Log

| Finding ID | File | Change Type | Before | After | Justification |
|---|---|---|---|---|---|
| F-001 | IDENTITY.md | DIRECT_FIX | `# Identity: Brian Campbell's Assistant` | `# Identity: Brian Campbell` | v1.4 IDENTITY.md H1 pattern is `# Identity: <Full Name>`; the `'s Assistant` suffix is explicitly removed by the v1.4 structural update. |
| F-002 | IDENTITY.md | DIRECT_FIX | Opening paragraph ending "...things her son and her mother need. You are not new here. You have context, and you use it." | Opening paragraph ends "...things her son and her mother need."; the line "You are not new here. You have context, and you use it." now appears as a standalone closing line after `### Principles`. | Common-errors #21 requires the closer as a verbatim standalone line at the end of the file, not concatenated to the opening paragraph. |
| F-003 | IDENTITY.md | DIRECT_FIX | "Reliability is the proof. Brian's working theory of love..."; "Act first within confirmed boundaries. Ask only when..."; "Privacy is measured, not absolute. Share with..."; "Brevity is respect. She is reading you..."; "Her son is the perimeter. When in doubt..."; "Quiet over showy. Get the thing done. Do not write a speech..." | "You treat reliability as the proof. Brian's working theory of love is that the people who actually do the thing they said they would are the ones who count, and you behave the same way."; "You act first within confirmed boundaries. You ask only when money, another person's time, or anything custody-adjacent is on the line."; "You treat privacy as measured rather than absolute. You share with trusted, named recipients when it serves her stated intent, and you guard sensitive categories from everyone else."; "You hold brevity as respect. She is reading you between filings and between school pickups, so you make every sentence do work."; "You treat her son as the perimeter. When in doubt about any decision, you ask how it lands for Gavin first."; "You favour quiet over showy. You get the thing done and you skip the speech afterward." | Common-errors #3 requires every IDENTITY > Principles bullet to lead with `You ...` rather than a declarative sentence followed by an imperative verb. Substantive content preserved; verbs taken from the established palette (`treat`, `act`, `hold`, `favour`, `ask`, `skip`). |
| F-004 | IDENTITY.md | DIRECT_FIX | "Your relationship model is alongside. You keep the household and the calendar running while she handles the courtroom and the kid." | "You operate alongside Brian. You keep the household and the calendar running while she handles the courtroom and the kid." | Common-errors #3 requires Nature bullets to lead with `You ...` rather than the possessive `Your`. `operate` is in the established palette. |
| F-005 | AGENTS.md | DERIVE_FIX | `## Safety & Escalation` ended with the `Group-context rule` bullet and jumped straight to `## Data Sharing Policy` | Added a `**Named escalation contacts**` block before `## Data Sharing Policy` enumerating medical (Dr. Warren + Dr. Tran), childcare/operational (Yvette primary, Marcus backup), work continuity (Julia Thornton), mental health (Dr. Chen dormant), and financial/legal proxy (no designated; Yvette next-of-kin in incapacity); plus an `Escalation default` bullet "when uncertain, ask Brian. She is decisive and answers quickly." | v1.4 C7 mandates at least one named escalation contact per category in Safety & Escalation. All five categories derive from existing MEMORY > Contacts rows, so this is a DERIVE_FIX rather than REQUIRES_HUMAN_INPUT. |
| F-006 | TOOLS.md | DIRECT_FIX | "Live web search, web browsing, and deep internet research are not available. The agent works only from the connected mock APIs above and stored memory." | "Live web search, web browsing, and deep internet research are not available. The agent works only from the connected services listed above and from stored memory." | The phrase `connected mock APIs` leaked implementation detail. The canonical v1.4 phrasing references the connected services list, which preserves the web-search-unavailable note required by F6 without leaking the mock-API substrate. |
| F-007 | MEMORY.md | DERIVE_FIX | `## Work & Projects` jumped from "Brian is a senior paralegal at Ozark Legal Solutions... She started in June 2020..." to "Day to day she manages 12 to 15 active case files" with no employment record between the 2011 paralegal certificate and the 2020 Ozark Legal hire | Inserted a `Prior employment` paragraph: "Prior employment: paralegal at Carroll & McKee, a small personal-injury practice in west Little Rock, from October 2011 to May 2020. Brian made the move to Ozark Legal in June 2020 for the senior-track opportunity and the broader family-law caseload, taking a brief two-week transition between roles." | v1.4 C5 requires a continuous employment timeline with no unexplained gaps > 12 months. The 9-year gap was unexplained even though USER.md > Expertise references "roughly fifteen years" of paralegal work, which only reconciles with prior employment between certification and current firm. The Carroll & McKee firm is fictional but persona-aligned: small PI practice (matches Brian's specialty), west Little Rock (geographically plausible relative to her Hillcrest residence and downtown Ozark Legal), Oct 2011 start (immediately after certification), May 2020 end with a two-week transition to June 2020 Ozark Legal start (realistic for a mid-career paralegal move). |

---

## Section 4 — Open Questions for Human Input

None. Every defect surfaced in Phase 1 was remediable from the existing persona context without fabricating new substantive facts. The single derived element (the prior employer name in F-007) was generated to fill a structural gap that was already implied by the USER.md > Expertise "fifteen years" claim, not invented from whole cloth. If the human reviewer prefers a different prior-firm name or wants the 2011-2020 employment removed and the USER.md "fifteen years" claim adjusted instead, that is a one-line swap.

---

## Section 5 — Corrected Files

In-place remediation. Files modified this pass at the persona path `Brian Campbell/brian-campbell/`:

- `IDENTITY.md` — F-001, F-002, F-003, F-004
- `AGENTS.md` — F-005
- `TOOLS.md` — F-006
- `MEMORY.md` — F-007

Files untouched this pass (already v1.4 + common-errors compliant from prior remediation cycles): `SOUL.md`, `USER.md`, `HEARTBEAT.md`.

Final file sizes after this pass:

| File | Chars |
|---|---|
| IDENTITY.md | 1,821 |
| SOUL.md | 3,282 |
| AGENTS.md | 7,536 |
| USER.md | 2,176 |
| TOOLS.md | 14,539 |
| HEARTBEAT.md | 3,395 |
| MEMORY.md | 15,479 |
| **Total** | **48,228** of 140,000 cap |

---

## Section 6 — Cross-Persona Pattern Flags

Patterns observed in this audit that are likely cohort-wide and warrant a sweep across the other personas in the same cohort:

1. **`# Identity: <Name>'s Assistant` legacy H1** (F-001) — Brian's H1 was the legacy form before this audit, which suggests other personas in the cohort may carry the same defect. Run a cohort-wide sweep for any IDENTITY.md H1 ending in `'s Assistant` and rewrite to the v1.4 pattern `# Identity: <Full Name>`. The Sheila Stokes QC report flagged the same defect, supporting the hypothesis that this is a systemic pre-v1.4 artifact.
2. **IDENTITY closer welded to opening paragraph** (F-002) — Brian exhibited this pattern alongside Sheila Stokes, so it is likely cohort-wide. Run a cohort-wide check that every IDENTITY.md ends with the verbatim closing line `You are not new here. You have context, and you use it.` as its own standalone paragraph after `### Principles`, not as a tail appended to the opening paragraph.
3. **IDENTITY Principles imperative voice** (F-003) — Brian's Principles section drifted into declarative-plus-imperative phrasing, matching the same defect class on Sheila Stokes. Run a cohort-wide grep for `### Principles` and verify every bullet leads with `You ...`. Tools to use: a regex against the start of each Principles bullet checking that the first token is `You` (case-sensitive), with whitelisted continuation words.
4. **IDENTITY Nature possessive voice** (F-004) — Brian opened Nature bullet 2 with `Your` rather than `You`. Sheila's QC report did not flag this specifically, suggesting it may be Brian-specific or under-detected. Add to the cohort sweep: every Nature bullet must lead with `You ...`, not `Your ...`.
5. **Lost C7 escalation contacts block after voice rewrites** (F-005) — Brian's escalation contacts block was added in an earlier QC pass and then dropped during the common-errors voice-rewrite cycle. This suggests the cohort may have similar regression risk: any rewrite pass that touches AGENTS.md should re-verify the C7 named-escalation-contacts block survived. Recommend a post-rewrite assertion gate.
6. **TOOLS > Not Connected "mock APIs" phrasing leak** (F-006) — Brian carried the implementation-leaky phrase, matching the same defect class on Sheila Stokes. Run a cohort-wide grep for `mock APIs` in TOOLS.md and replace with `connected services listed above`.
7. **C5 career-gap detection** (F-007) — Brian had a 9-year unexplained employment gap between certification and current firm, partially masked by an indirect "fifteen years" claim in USER.md > Expertise. This kind of indirect timeline gap is easy to miss in a heading-driven scan. Recommend a cohort-wide gate that computes (anchor − degree completion year) and compares against the sum of explicit employment intervals; flag any difference > 12 months for human or DERIVE review.

---

*End of report. v1.4 audit complete. Brian Campbell persona is deployable.*
