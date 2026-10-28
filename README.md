# Problem Scout

Find real complaints. Bring the evidence to Problem Filter.

A Galvora Labs open-source product, delivered as a portable agent skill. Give it a niche or audience; it searches public complaints and produces evidence briefs you can paste into [Problem Filter](https://github.com/galvoralabs/problem-filter).

Finding the incident, workaround, and consequence is often the slowest part of problem discovery. Problem Scout does that research and shows its sources. Problem Filter handles the decision about an idea.

## What it returns

- A map of places searched and access limits.
- Numbered, dated incidents with public handles and source links.
- Pain themes with distinct people and thread counts.
- Strong, Medium, or Weak evidence ratings.
- Six-field briefs matching Problem Filter's input format.
- Candidate ideas tied to specific incidents, after the evidence.

Missing details remain **Not stated**. Unopened sources are **UNVERIFIED** and do not strengthen a theme. A weak or empty result is useful when the public evidence is scarce.

## Use it

Share this repository with your agent and ask it to read `SKILL.md`, or copy the single file into your agent's skill directory.

```text
Read SKILL.md and use problem-scout.
Niche: solo developers building and shipping agent skills.
Find first-person complaints, check the linked sources, and return evidence briefs.
```

Other example niches: small shop owners selling on Instagram in India; Obsidian users syncing notes across devices; Etsy sellers supporting digital downloads. These are research inputs, not claims of demand.

### Download the skill

[Download SKILL.md](https://raw.githubusercontent.com/galvoralabs/problem-scout/main/SKILL.md). Only this file is needed at runtime. The skill needs an agent with working web search and source-reading access; it has no hosted service, database, package dependencies, or separate API key. Your agent's browsing access and provider costs still apply.

### Native Agent Skills

| Agent | Project installation path | Example request |
| --- | --- | --- |
| OpenAI Codex | `.codex/skills/problem-scout/SKILL.md` | `Use problem-scout for [niche].` |
| Claude Code | `.claude/skills/problem-scout/SKILL.md` | `Use problem-scout for [niche].` |
| Google Antigravity | `.agents/skills/problem-scout/SKILL.md` | `Use problem-scout for [niche].` |

For another agent, provide the file directly and ask it to follow the instructions. If browsing is unavailable, paste source material; results must then say they are user-supplied rather than independently verified. Installation paths are documented as requested; native discovery has not been tested across all three agents.

## The evidence output

Each theme includes its evidence rating, independent source count, distinct people, and distinct threads. Every incident records who reported what, when, the workaround, and the consequence. The brief has these exact fields:

1. Person who experienced the problem.
2. A recent incident.
3. Current workaround and where it fails.
4. Cost, risk, delay or emotional consequence.
5. Existing products already tried.
6. Smallest outcome a first version should deliver.

The first five fields describe evidence; the sixth is a labelled proposed outcome. Unverified links, missing facts, resolved issues, and uncertain identities remain visible. Public accounts are self-reports, not independently authenticated customers, and source counts are not market-size estimates.

## Work with Problem Filter

1. Run Problem Scout on a niche.
2. Review the linked incidents and missing evidence.
3. Paste a brief into Problem Filter, with a candidate idea if desired.
4. Let Problem Filter assess the idea and explain any evidence gaps.

No automatic handoff, installation, or account connection is required. Scout rates evidence; Filter evaluates ideas.

## Proof

[TEST-REPORT.md](TEST-REPORT.md) records three manual research runs performed in Codex with real web access on 28 October 2026. The first niche was selected by the product owner for hand checking. The report includes full briefs, linked incidents, corrections found in follow-ups, and limitations. These are same-session product tests, not independent model evaluations or tests of every agent runtime.

## Product files

```text
problem-scout/
├── SKILL.md
├── README.md
├── LICENSE
└── TEST-REPORT.md
```

Built by **Galvora Labs**, as part of **20 Days / 20 Products**. Licensed under [MIT](LICENSE).
