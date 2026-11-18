# Methodology — The Combined Multi-Agent System

**Entry:** MecCog Challenge, Papers and Findings (Step 1) — five APOE4 / Alzheimer's disease hypotheses (H1–H5)
**Team:** Malikian Evidence Review (Raphael Malikian, solo entrant and team leader)
**Method URL:** https://github.com/rtmalikian/meccog-apoe4-evidence-review

## The system in one paragraph

This entry was produced by composing two open, previously published multi-agent systems by the same author into a single evidence pipeline. The first system — a **multi-agent Cochrane-level review process** — does the production work: searching, screening, extraction. The second — a **multi-agent peer review system** — does no production work at all; it exists to attack the first system's output: challenging each finding's direction, checking reporting and reproducibility, and running a final integrity gate that verifies every verbatim quote and every statistic's provenance against its source before anything is submitted. One human author sets the questions, adjudicates the disagreements the agents cannot settle by re-reading, and signs off every row. The novelty is the composition and the discipline it enforces: no finding reaches the submission on a single agent's say-so, every number carries a machine-checkable statement of where it came from, and disagreements are resolved by returning to the source text, never by vote or by plausibility.

## Why this is a different way to build an evidence submission

1. **Production and verification are separate systems.** Most automated or AI-assisted reviews use one pipeline and check its output, if at all, with the same process that made it. Here the checking system is an independent protocol with its own roles and gates, designed adversarially: one of its reviewers (the sceptic) is tasked with arguing *against* each finding's stated direction.
2. **Independence is structural, not requested.** Screening and verification passes run in separate sessions with no sight of each other's outputs. The second screener does not see the first screener's decisions; the integrity gate does not see the extractor's reasoning, only the rows and the sources.
3. **Every statistic is provenance-coded.** Each effect size, P value, and sample size carries one of a fixed set of provenance codes (printed in text, visual only, estimated from figure, supplement only, not found, full text unavailable, ambiguous panel), with consistency rules enforced across the row: a value marked unavailable must be recorded as N/A, and a P value is never estimated from a figure. Uncertainty is represented in the data, not smoothed over.
4. **Verbatim quotes are verified, not trusted.** Findings carry a verbatim quote from the source, and the integrity gate checks quotes against the source text (programmatically where the full text is machine-readable) before submission.
5. **Contradicting evidence is a first-class output.** Null and contradicting findings are extracted and labelled like any other finding, including findings that cut against the hypothesis as stated.
6. **Unresolvable disagreements are held out, not forced.** Where the two screening passes could not be reconciled by re-reading, the paper was excluded from the submission and recorded as disputed in the public screening files, rather than being pushed through on a judgement call.

## Pipeline

```
Hypothesis text (verbatim, as supplied by the challenge)
        |
[1] SEARCH        Information-specialist agent: per-hypothesis strings built from the
                  hypothesis's own mechanism terms; Europe PMC; two runs (Run 1 broad,
                  Run 2 excluding reviews/syntheses/editorials); top 200 per run screened.
        |
[2] SCREENING     Screener A (inclusion pass) + Screener B (independent verification pass),
                  separate sessions. Eligibility: experimental studies directly testing
                  APOE4 vs APOE3/APOE2 (or APOE4 manipulation) on the hypothesis mechanism.
        |
[3] ADJUDICATION  Borderlines and disagreements settled by re-reading the source.
                  Unreconcilable papers held out as disputed (9 across H1-H5) and logged.
        |
[4] EXTRACTION    Per finding: description, verbatim quote, arrow-form summary,
                  relevance 0-1, experimental system, panel-level data location,
                  effect size / P value / sample size each with a provenance code,
                  directness class and strength (Moult scale, see below).
        |
[5] PEER REVIEW   Panel from the second system: domain reviewer, reporting and
                  reproducibility reviewer, and a sceptic arguing against each
                  finding's stated direction.
        |
[6] GATE 6        Integrity gate: every verbatim quote checked against its source;
                  provenance-consistency rules checked across every row; DOIs checked
                  against their records (two wrong DOIs in first-pass records were
                  caught and corrected at this stage; one paper with no verifiable
                  DOI anywhere is recorded as N/A rather than assigned a guessed DOI).
        |
[7] HUMAN         The author re-reads flagged quotes and a sample of unflagged rows,
    SIGN-OFF      adjudicates what remains, and signs off each spreadsheet.
        |
   Submission spreadsheets (validated with the challenge's official validator)
```

## Agent roles

All roles run on one model (Muse Spark, Meta) driven through the Muse personal-agent environment. Roles differ by prompt, persona, and session isolation, not by model; no more precise build identifier is exposed to the operator, so none is claimed.

| Role | System | Job |
|---|---|---|
| Information specialist | Review process | Builds per-hypothesis search strings from the mechanism terms; keeps the search log, including searches that returned nothing usable |
| Screener A | Review process | First inclusion pass over titles/abstracts against the eligibility criterion |
| Screener B | Review process | Independent verification pass; checks Screener A's inclusions and exclusions without seeing its reasoning; caught two wrong DOIs and three non-isoform-specific inclusions in this run |
| Adjudicator | Review process | Settles screening disagreements by re-reading the source; holds out papers that cannot be reconciled |
| Extractor | Review process | Builds the finding rows: quote, summary, statistics with provenance, directness scoring |
| Sceptic reviewer | Peer review system | Argues against each finding's stated direction; responsible for contradicting/null findings being recorded as such |
| Domain reviewer | Peer review system | Challenges mechanistic fit: does this experiment actually test the hypothesis's A and B? |
| Reporting / reproducibility reviewer | Peer review system | Challenges completeness: missing statistics, vague data locations, unverifiable claims |
| Gate 6 integrity checker | Peer review system | Verifies every verbatim quote against the source text and every row against the provenance-consistency rules |
| Human author | — | Sets the questions, adjudicates what the agents cannot settle, re-reads flagged material, signs off; accountable for every row |

## Directness scoring

Directness follows the challenge's own document (Moult, *Directness of Evidence* v02): class 1 where the hypothesis's A itself is perturbed or naturally varying and B itself is measured; class 2 for an indirect input (surrogate A′); class 3 for an indirect output (surrogate B′); class 4 where both are surrogates; class 5 otherwise, with the reason stated in the finding description. Strength (1 very strong – 5 very weak) is scored alongside the class.

## What this run produced

- 82 papers and 152 findings across the five hypotheses (H1: 14 papers / 28 findings; H2: 24 / 34; H3: 11 / 24; H4: 17 / 33; H5: 16 / 33).
- 17 papers were abstract-only; every statistic that could not be verified from the reachable text carries the `full_text_unavailable` provenance rather than an invented value.
- Contradicting and null findings are included and labelled (among them: no isoform effect on amyloid-β synthesis in one included study; no production effect in mouse neurons in another; no significant APOE4 effect on synaptic markers in human organoids, recorded with its P value).
- 9 papers on which the two screening passes disagreed irreconcilably were held out and are listed, with reasons, in the public screening files — a candidate list for a later full-text adjudication pass.

## Reproducibility

Everything needed to audit or rerun this method is public:

- This repository: per-hypothesis method notes (`methods/`), the full screening records including held-out disputed papers (`screening/`), the extraction data the spreadsheets were built from (`extraction/`), both search logs (`search-logs/`), and the validated submission spreadsheets (`submissions/`).
- The two protocols, including their full prompt sets: [Multi-Agent Cochrane-Level Review Process](https://github.com/rtmalikian/multi-agent-cochrane-level-review-process) and [Multi-Agent Peer Review System](https://github.com/rtmalikian/multi-agent-peer-review-system-clinical-ai-medical-research).
- Each submission spreadsheet's Method sheet pins the exact commit of this repository its rows were built from.

## Known limitations

- A single human author adjudicates and signs off; there is no second human reviewer.
- All agent roles run on one underlying model. Diversity between roles comes from prompts, personas, and session isolation; whether persona diversity outperforms repeated single-persona review is an open question the author has pre-registered an evaluation for in the peer review system's repository, and it is not claimed as proven here.
- Abstract-only papers limit what can be verified; the provenance codes make that limit visible row by row rather than hiding it.
- The evidence base for some sub-claims is thin (notably barrier-specific ABCA1 transport in H1); the submissions state this rather than filling the gap with weaker, off-mechanism papers.

---

Malikian R. MecCog Challenge APOE4 Evidence Review: combined multi-agent Cochrane-level review and peer review method. 2026–2027. GitHub: https://github.com/rtmalikian/meccog-apoe4-evidence-review · ORCID: 0009-0008-4326-4205
