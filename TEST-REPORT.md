# Problem Scout — Codex Research Test Report

## Method and limits

Three real, manual research runs in this Codex desktop conversation on **2026-10-28**, using the drafted `SKILL.md`, web search/open, and the connected GitHub reader. The 18-calendar-month cutoff was **2025-04-28**. Sources were discovered through complaint searches, then reopened and read with follow-ups. This report contains the resulting evidence briefs, not simulated output or invented fixtures. No independent agent or native installation was tested.

The product owner selected **solo developers building and shipping agent skills** as the niche they can check by hand. Public handles establish attribution, not verified identity or occupation. Whether those reporters work solo is not established. This is a coverage gap, not an assumed fact.

Counts below cover only the explicitly selected affected reporters. Comments, votes, bots, and suspected duplicates do not become extra independent sources. Each theme is intentionally narrow; these runs found mostly Weak evidence. No build verdict is implied. All statements are paraphrases; no direct quotations are used. Proposed outcomes and candidate ideas are inferences.

## Run 1 — Solo developers building and shipping agent skills

**Input:** Use problem-scout to find real problems experienced by solo developers building and shipping agent skills.

**Complaint venues mapped:** GitHub issues; r/ClaudeCode; r/claudeskills; r/ClaudeAI; Cursor community forum; Hacker News; personal developer incident write-ups.

**Queries used:** `site.reddit.com/r/ClaudeAI skills "workaround" "2026"`; `site.github.com/anthropics/claude-code/issues skills "workaround" "2026"`. Searches also surfaced developer write-ups, forum posts, issue mirrors, and aggregators. The three source threads below were fetched directly through GitHub along with their comments. Secondary mirrors and generic explanations were not counted.

**Coverage limit:** Selected evidence comes from one product's GitHub tracker. Solo status is unconfirmed; this run demonstrates extraction and qualification, not complete niche coverage. The tool reader retrieved current issue state and comment updates, exposing two misleading first impressions.

### User-level skills disappear from discovery | Weak | 1

Counts: 1 verified independent source; 1 person; 1 thread.

Incidents:
1. **I01** — [GitHub issue 38051](https://github.com/anthropics/claude-code/issues/38051), **2026-03-24**, **tlvenn**, a Claude Code user managing skill files in dotfiles. User-level skills did not appear while project-level skills loaded. Replacing symlinks with copied directories did not restore discovery. Consequence: personal skills remained unavailable despite troubleshooting. Existing product: Claude Code 2.1.81. Status: reporter closed the issue after withdrawing the symlink diagnosis; closure did not establish a fix. [Author correction](https://github.com/anthropics/claude-code/issues/38051#issuecomment-4114951145) read. Verified **2026-10-28** through GitHub issue and comments API.

Brief for problem-filter:
1. Person who experienced the problem: tlvenn, user-level skill author/user; solo status not stated. [I01]
2. A recent incident: skill discovery failed on 2026-03-24. [I01]
3. Current workaround and where it fails: copied real directories still did not load. [I01]
4. Cost, risk, delay or emotional consequence: unavailable skills and repeated setup troubleshooting; duration not stated. [I01]
5. Existing products already tried: Claude Code 2.1.81. [I01]
6. Smallest outcome a first version should deliver: explain why one installed skill is absent from discovery (proposed inference).

Missing evidence: current reproducibility and the real cause; whether the reporter works solo.

### Forked skills lose interactive questions | Weak | 1

Counts: 1 verified independent source; 1 person; 1 thread. Historical incident with a later reported fix; not evidence of a current defect.

Incidents:
2. **I02** — [GitHub issue 54892](https://github.com/anthropics/claude-code/issues/54892), **2026-04-30**, **tmchow**, author of an affected skill. On Claude Code 2.1.123/macOS, a forked skill did not invoke AskUserQuestion despite allowed-tools. Removing `context: fork` restored interaction but sacrificed isolation. Consequence: skipped/plain-text questions or lost isolation. Status: closed as duplicate; an automated maintainer comment [reports a fix in 2.1.126](https://github.com/anthropics/claude-code/issues/54892#issuecomment-4357786969). Fix not independently reproduced. Verified **2026-10-28** through issue and comments API. A speculative non-author comment was excluded from evidence counts.

Brief for problem-filter:
1. Person who experienced the problem: tmchow, affected skill author; solo status not stated. [I02]
2. A recent incident: interactive tool unavailable in a forked skill on 2026-04-30. [I02]
3. Current workaround and where it fails: remove fork mode, losing context isolation. [I02]
4. Cost, risk, delay or emotional consequence: an intended interaction failed silently; isolation trade-off. [I02]
5. Existing products already tried: Claude Code 2.1.123 on macOS. [I02]
6. Smallest outcome a first version should deliver: detect a skill's unavailable runtime tools before relying on them (proposed inference).

Missing evidence: any recurrence after the reported fix; time spent; solo status.

### Skill activation needs manual suppression | Weak | 1

Counts: 1 verified independent source; 1 person; 1 thread.

Incidents:
3. **I03** — [GitHub issue 45225](https://github.com/anthropics/claude-code/issues/45225), **2026-04-08**, **justanotherkevin**, user customizing skill activation. Adding `disabledSkills` to settings was rejected. The reporter built a flag file, prompt hook, toggle script, and custom status indicator to suppress a skill group. Consequence: managing extra scripts/settings to control unexpected activation. This is a reported working workaround, not evidence that it fails. Status: closed automatically as duplicate of 43928, with no fix established by this thread. Verified **2026-10-28** through issue and comments API.

Brief for problem-filter:
1. Person who experienced the problem: justanotherkevin, skill user/customizer; solo status not stated. [I03]
2. A recent incident: settings rejected an attempted skill-disable option on 2026-04-08. [I03]
3. Current workaround and where it fails: custom hook/toggle/status scripts; failure not stated. [I03]
4. Cost, risk, delay or emotional consequence: extra manual setup and uncertainty about activation; numeric cost not stated. [I03]
5. Existing products already tried: Claude Code settings, hooks, and superpowers skills. [I03]
6. Smallest outcome a first version should deliver: show and control the activation state of a selected skill group (proposed inference).

Missing evidence: failure of the current workaround and current native support; solo status.

Candidate ideas (inferences, after the evidence):
- Skill discovery diagnostic checklist explaining the installed-versus-discovered difference. [I01](https://github.com/anthropics/claude-code/issues/38051)
- Runtime capability smoke-check for interactive skills; account for the reported fix. [I02](https://github.com/anthropics/claude-code/issues/54892)
- Visible skill-group activation switch. [I03](https://github.com/anthropics/claude-code/issues/45225)

**Observed result:** Three complete six-field brief structures; missing facts preserved; withdrawn diagnosis and reported fix retained. Public evidence does not confirm the solo-developer audience restriction.

Next: run problem-filter on these briefs.

## Run 2 — Obsidian users syncing across devices

**Input:** Use problem-scout for Obsidian users who switch between desktop and mobile devices.

**Complaint venues mapped:** Obsidian Help forum; Obsidian Bug Reports; r/ObsidianMD; r/selfhosted; sync-plugin GitHub issues; mobile app-store reviews; Hacker News.

**Queries used:** `site.reddit.com/r/ObsidianMD mobile sync "2025" "lost"`; `site.forum.obsidian.md "2025" "sync" "workaround" "lost"`; `site.forum.obsidian.md "2025" "sync" "workaround"`.

**Coverage limit:** Three opened first-person forum threads selected; no authenticated app-store review access exercised. Old loss reports were not promoted on the basis of crawl date. These themes concern separate workflows; they do not establish one shared sync defect.

### Switching machines before changes arrive | Weak | 1

Counts: 1 verified independent source; 1 selected affected person; 1 thread.

Incidents:
4. **I04** — [Obsidian forum](https://forum.obsidian.md/t/realtime-sync-or-possibility-to-explicitly-trigger-sync/104717), **2025-08-25**, **binaryanomaly**, user of multiple computers and mobile devices. Changes had not uploaded/downloaded when switching machines. Workaround: wait or close/reopen/reload the app. Consequence: waiting before continuing. An August 27 follow-up says this mainly affects laptop/desktop switching; do not recast it as primarily mobile. Other people's status-icon advice is not the author's tested workaround. No later fix confirmed in the opened thread. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: binaryanomaly, multi-device Obsidian user. [I04]
2. A recent incident: reported delayed sync during device switching on 2025-08-25. [I04]
3. Current workaround and where it fails: waiting or reopening; no quantified success rate stated. [I04]
4. Cost, risk, delay or emotional consequence: interruption and waiting between computers; duration not stated. [I04]
5. Existing products already tried: Obsidian sync workflow. [I04]
6. Smallest outcome a first version should deliver: make upload/download completion clear before switching (proposed inference).

Missing evidence: delay duration, reproducibility on current versions, actual workaround failure rate.

### Moving to native Sync breaks quick capture | Weak | 1

Counts: 1 verified independent source; 1 person; 1 thread.

Incidents:
5. **I05** — [Obsidian forum](https://forum.obsidian.md/t/workaround-to-use-drafts-to-append-to-daily-note-in-obsidian-using-obsidian-sync/104789), **2025-08-26**, **nrenfree**, Drafts/Obsidian user switching from iCloud to native Sync. Previously convenient daily-note appending no longer worked in their setup. Reconfiguring integration did not help; current workaround is capturing in Drafts and copying into Obsidian at day's end. Consequence: an added transfer step and delayed consolidation. General Sync was reported better. Topic auto-closed after inactivity, not confirmed solved. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: nrenfree, Drafts and Obsidian user. [I05]
2. A recent incident: quick capture integration stopped working after a sync migration, reported 2025-08-26. [I05]
3. Current workaround and where it fails: daily copy/paste; restores transfer but loses immediate appending. [I05]
4. Cost, risk, delay or emotional consequence: manual transfer and end-of-day delay; minutes not stated. [I05]
5. Existing products already tried: Drafts, iCloud, Obsidian Sync, integration reconfiguration. [I05]
6. Smallest outcome a first version should deliver: append a captured Drafts entry to the intended daily note (proposed inference).

Missing evidence: current reproducibility, exact setup, measured transfer effort.

### Workspace layouts require repeated setup | Weak | 1

Counts: 1 verified independent source; 1 selected affected person; 1 thread. Several other handles appear in this thread; none increases the independent thread count.

Incidents:
6. **I06** — [Obsidian forum](https://forum.obsidian.md/t/workspaces-obsidian-sync/105023), **2025-08-31**, **Kaleo**, multi-device workspace user. Saved layout effort did not carry across devices. A **2026-03-31** follow-up still describes repeated setup on each device. Workaround: redo layouts; consequence: repeated time spent. Other users discuss both cross-device rendering and merge problems; these are not proven to share a cause. No resolution confirmed. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: Kaleo, multi-device Obsidian user. [I06]
2. A recent incident: workspace sync complaint on 2025-08-31, reaffirmed 2026-03-31. [I06]
3. Current workaround and where it fails: repeat setup on devices, losing the benefit of shared layouts. [I06]
4. Cost, risk, delay or emotional consequence: repeated configuration effort; duration not stated. [I06]
5. Existing products already tried: Obsidian Workspaces and Sync. [I06]
6. Smallest outcome a first version should deliver: preserve a named workspace's intended tabs/layout across specified devices (proposed inference).

Missing evidence: clean reproduction, device combination, actual time cost.

Candidate ideas (inferences, after the evidence):
- Device-switch sync completion check. [I04](https://forum.obsidian.md/t/realtime-sync-or-possibility-to-explicitly-trigger-sync/104717)
- Drafts-to-daily-note transfer action. [I05](https://forum.obsidian.md/t/workaround-to-use-drafts-to-append-to-daily-note-in-obsidian-using-obsidian-sync/104789)
- Named workspace preservation/export helper. [I06](https://forum.obsidian.md/t/workspaces-obsidian-sync/105023)

**Observed result:** Three briefs preserve actual workaround limitations. A successful manual workaround was not labelled total failure, and other users' experiences were not merged into Kaleo's account.

Next: run problem-filter on these briefs.

## Run 3 — Etsy sellers supporting digital orders

**Input:** Use problem-scout for Etsy sellers handling digital downloads and customer support.

**Complaint venues mapped:** r/EtsySellers; r/Etsy; r/EtsyDigitalSeller; Etsy Technical Issues forum; Etsy seller app reviews; Canva community; niche craft seller forums.

**Queries used:** `site.reddit.com/r/EtsySellers "digital" "2025" "download" "annoying"`; `site.reddit.com/r/EtsySellers "digital" "workaround" after:2025-04-28`; `Etsy sellers digital downloads customers cannot download reddit 2025 2026 complaints`. Broader complaint search succeeded after restrictive queries returned unrelated material.

**Coverage limit:** Reddit threads opened; precise dates came from search-indexed dated thread content matched to the opened posts. No private seller data or order history inspected. Undated review aggregations and pre-cutoff complaints were excluded. Forum previews behind login were not treated as verified incidents. Customers' alleged causes remain seller accounts, not proven Etsy defects.

### Buyers cannot locate delivered files | Medium | 2

Counts: 2 verified independent sources; 2 selected people; 2 threads. No prevalence or quantified support cost established.

Incidents:
7. **I07** — [Reddit thread](https://www.reddit.com/r/Etsy/comments/1r4hhjz/anyone_else_getting_tired_of_being_a_tech_support/), **2026-02-14**, **AgeKlutzy2283**, digital asset seller. Buyers repeatedly asked about download access despite listing instructions. Workaround: saved replies and Etsy help links; the author still received follow-ups. Consequence: frustration with repeated explanations. Counterevidence: other sellers in the thread report quick replies work well. Verified **2026-10-28**.
8. **I08** — [Reddit thread](https://www.reddit.com/r/Etsy/comments/1lgsv7t/), **2025-06-21**, **CaityBunches**, digital file seller. Guest customers repeatedly could not find files. The seller tested the purchase email flow and later confirmed emailing files when needed. Consequence: recurring manual support. Cause unproven; do not prescribe self-purchasing from this account as a validation method. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: AgeKlutzy2283, digital asset seller. [I07]
2. A recent incident: repeated access questions reported 2026-02-14. [I07]
3. Current workaround and where it fails: listing instructions, saved replies, help links; follow-ups continue. [I07]
4. Cost, risk, delay or emotional consequence: frustration and repeated explanations; time/cost not measured. [I07]
5. Existing products already tried: Etsy listing guidance, saved replies, Etsy help. [I07]
6. Smallest outcome a first version should deliver: give a buyer the correct file-access instructions for their checkout/device (proposed inference).

Missing evidence: support minutes per order, effectiveness against existing saved replies, current recurrence.

### File-format confusion damages ratings | Weak | 1

Counts: 1 verified independent source; 1 selected person; 1 thread.

Incidents:
9. **I09** — [Reddit thread](https://www.reddit.com/r/EtsyDigitalSeller/comments/1w3dh66/kinda_want_to_cry/), **2026-08-31**, **Upstairs-Tennis-3247**, PNG/SVG clipart seller. A buyer downloaded PNGs and complained that colours were not editable, leaving five one-star reviews. Seller explained SVGs and contacted support. Update: buyer eventually downloaded SVGs after a week, but reviews remained. Seller reports shop rating fell from five stars to 3.6. This is a self-reported rating change, not verified shop data. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: Upstairs-Tennis-3247, clipart seller. [I09]
2. A recent incident: file-format misunderstanding and negative reviews reported 2026-08-31. [I09]
3. Current workaround and where it fails: listing explanations, direct help and support contact; corrected download did not remove reviews. [I09]
4. Cost, risk, delay or emotional consequence: reported rating reduction to 3.6 and distress. [I09]
5. Existing products already tried: Etsy listing text/photos and support; PNG/SVG formats. [I09]
6. Smallest outcome a first version should deliver: help a buyer select the editable file before using the wrong format (proposed inference).

Missing evidence: verified shop data and whether better guidance changes outcomes.

### Troubleshooting unfamiliar customer devices | Weak | 1

Counts: 1 verified independent source; 1 selected person; 1 thread.

Incidents:
10. **I10** — [Reddit thread](https://www.reddit.com/r/Etsy/comments/1sy8qmg/just_have_to_vent/), **2026-04-28**, **13chemicals**, digital template seller using a PC. A buyer had a Mac/Canva issue the seller could not reproduce. Seller referred them to Canva support and received a one-star review. Consequence: anger and a negative review. Follow-up says customer questions are uncommon across the seller's large sales history; do not infer frequent pain. Another comment's shop-closure story dates from before Canva and was excluded as an undated historical incident. Verified **2026-10-28**.

Brief for problem-filter:
1. Person who experienced the problem: 13chemicals, PC-based template seller. [I10]
2. A recent incident: customer Mac issue followed by a one-star review, reported 2026-04-28. [I10]
3. Current workaround and where it fails: referral to Canva support did not prevent the review. [I10]
4. Cost, risk, delay or emotional consequence: negative review and anger; financial impact not stated. [I10]
5. Existing products already tried: Canva template on PC and support referral. [I10]
6. Smallest outcome a first version should deliver: collect device/browser facts and give a clear support handoff (proposed inference).

Missing evidence: actual fault, support outcome, economic impact; frequency appears low for this reporter.

Candidate ideas (inferences, after the evidence):
- Buyer file-access guide keyed to device and checkout type. [I07](https://www.reddit.com/r/Etsy/comments/1r4hhjz/anyone_else_getting_tired_of_being_a_tech_support/), [I08](https://www.reddit.com/r/Etsy/comments/1lgsv7t/)
- PNG/SVG chooser with a small editing demonstration. [I09](https://www.reddit.com/r/EtsyDigitalSeller/comments/1w3dh66/kinda_want_to_cry/)
- Customer device diagnostic intake and support handoff template. [I10](https://www.reddit.com/r/Etsy/comments/1sy8qmg/just_have_to_vent/)

**Observed result:** Three themes, with two threads clustered for file access. Other comments did not inflate counts. Rare incidents and useful existing workarounds remain visible.

Next: run problem-filter on these briefs.

## Acceptance review

| Check | Observed result |
| --- | --- |
| Three real niche runs in Codex | Completed in this session; not independently executed agents |
| Skill package validation | Bundled skill-creator quick_validate.py passed; SKILL.md is 81 lines, below 150 |
| Familiar niche selected by owner | Agent-skill developers; hand review still pending |
| Incident links open and support attribution | 10/10 selected incident URLs read; GitHub via connected issue reader, Reddit/forum via web open |
| Follow-up correction links | Both linked GitHub comments read through comments API |
| Quotes | Zero direct quotes; attributed paraphrases throughout |
| Recent evidence | All selected incidents on/after 2025-04-28; updates/resolutions retained |
| Distinct-source counts | 1 per theme except Etsy file access (2); no votes/comment inflation |
| Brief handoff | Nine six-field briefs use Problem Filter README field order; no reformatting needed |
| Evidence completeness | Partial: numeric costs, workaround failures, or audience identity are sometimes absent and explicitly marked |
| Product judging | No build/reject verdicts; candidate ideas labelled inferences |

The source-opening check passed in this environment at the time of the run. It does not guarantee later link availability or authenticate the stories. The briefs are structurally paste-ready; missing evidence can still lead Problem Filter to request more evidence. A downstream Problem Filter evaluation was not run because this product test concerns scouting, not judging ideas.

Observed refinements added to the skill: read follow-ups before accepting a diagnosis; preserve resolutions; separate distinct people from distinct threads; never splice multiple reporters into one brief; keep proposed outcomes separate from facts; explain coverage gaps.
