# MecCog Challenge — APOE4 Evidence Review: Combined Method

**Team:** Malikian Evidence Review (Raphael Malikian, solo entrant and team leader)
**Challenge:** [MecCog Challenge](https://huggingface.co/spaces/MecCog/meccog-challenge) — Papers and Findings, Step 1: connect five hypotheses about APOE4 and Alzheimer's disease risk to experimental evidence in published papers.
**Hypotheses covered:** the challenge's five official Step 1 statements, all endosome mechanisms: H1 (reduced endosome pH), H2 (impaired ARF6-related receptor recycling), H3 (APOE4 aggregation in the endo-lysosome), H4 (APOE4 adhesion to recycling receptors), H5 (lipid metabolism and late endosome function). The verbatim statements are in each submission spreadsheet (cell A2) and each `methods/` note.

This repository is the public method record for the entry. The method combines two open protocols by the same author, used together:

1. **Production pipeline** — [Multi-Agent Cochrane-Level Review Process (Robust Standard v2)](https://github.com/rtmalikian/multi-agent-cochrane-level-review-process): protocol-first searching, dual independent screening and extraction, adjudication by re-reading, and full reporting of agreement and discrepancy rates.
2. **Quality gate** — [Multi-Agent Peer Review System for Clinical AI, Medical Research and Health Technology Papers](https://github.com/rtmalikian/multi-agent-peer-review-system-clinical-ai-medical-research): persona-based reviewers and looped editorial gates, ending in a final integrity gate (Gate 6) that verifies every citation and quote against its source before anything is submitted.

Per-hypothesis method files (`methods/H1.md` … `methods/H5.md`), search logs (`search-logs/`), and the validated submission spreadsheets (`submissions/`) are committed here as each hypothesis is worked, so the record of what was actually done sits next to this description of the method.

## Why a multi-agent system — the appeal of this method

The point of this entry is the method as much as the findings. A conventional review, human or AI-assisted, is one pipeline checked, if at all, by the same process that produced it. This entry composes two separate multi-agent systems against each other: the review system produces the evidence, and the peer review system — which does no production work — attacks it, with a dedicated sceptic arguing against each finding's direction and a final integrity gate verifying every verbatim quote and every statistic's provenance against its source. Agent roles work in isolated sessions so verification is structurally independent, disagreements are settled by re-reading the source rather than by vote, papers the screeners cannot reconcile are held out publicly instead of forced through, and every number in the submission carries a machine-checkable provenance code stating exactly where it came from — or that it could not be found. The full methodology, including the pipeline, the agent role table, and the known limitations, is in **[METHODOLOGY.md](METHODOLOGY.md)**.

---

# Method

MecCog Step 1 submission.

- **Team:** Malikian Evidence Review
- **Hypothesis:** H1–H5 (shared method; hypothesis-specific detail in `methods/`)
- **Submission date:** January 2027 (deadline January 15, 2027)

## 1. Who did the work

One human author and a team of AI agents. The human author (Raphael Malikian) set the questions, adjudicated disagreements, and signs off every spreadsheet; he is accountable for every row.

The agents worked under the two protocols linked above. Within the Cochrane-level process, separate agent passes acted as: information specialist (search strings and search log), two independent screeners, a screening adjudicator, two independent extractors, a settlement reader, and a methods editor. Within the peer review system, a separate panel — including a domain reviewer, a reporting/reproducibility reviewer, and a sceptic whose job is to argue against each finding's stated direction — challenged the completed extraction for each hypothesis, and the Gate 6 integrity pass verified every verbatim quote against the source text before submission. Screening and extraction passes ran in separate sessions with no sight of each other; disagreements were settled by re-reading the source, never by a rule.

## 2. Model and version

All agent passes ran on Muse Spark (Meta), driven through the Muse personal-agent environment. One model was used for every agent role; the roles differ by prompt, persona, and session isolation, not by model. No more precise build identifier is exposed to the operator, so none is claimed here.

## 3. How papers were found

Europe PMC, searched per hypothesis with strings built from the official statement's own mechanism terms (endosomal pH and acidification for H1; ARF6 and receptor recycling for H2; aggregation in the endo-lysosomal system for H3; recycling receptors, retromer and sortilin for H4; cholesterol, lipid metabolism and lysosomal function for H5), limited to experimental studies, in two runs (the second excluding reviews, syntheses and editorials). The challenge's five starting references were fetched explicitly by PMID; one of them (Kaji 2024, H3) was absent from both search runs and was resolved by full-text adjudication. A supplementary looser search for H3 found no new candidates. The exact string, date, source, and hit count for every search are recorded per hypothesis in `search-logs/`. Note: an earlier build of this entry used incorrect hypothesis statements and was replaced before submission — see `CORRECTION-2026-11-18.md`.

## 4. How full text was obtained

Open-access publisher versions and PubMed Central first, then the DOI landing page. Where only the abstract was reachable, a finding drawn from it is located as "Abstract" in the submission and its directness is scored on that basis. Papers with no reachable text contribute no rows; they are counted in the per-hypothesis search log as not retrieved rather than silently dropped.

## 5. What a human checked

The Gate 6 integrity pass (an agent pass under the peer review protocol) verified every verbatim quote against the source text and every DOI against its record. The human author personally re-read every quote the integrity pass flagged, re-read a sample of the unflagged rows for each hypothesis, adjudicated every screening and extraction disagreement the agents could not settle by re-reading, and signed off each spreadsheet before it was submitted.

## 6. Anything else

Directness class and strength are scored using the challenge's own document, John Moult's *Directness of Evidence* (v02). Known weaknesses: a single human author; agent extraction can misread context in dense results sections, which the dual-extraction and verbatim-quote requirements are there to catch; and the evidence base for the narrowest statements is thin — H3 confirms a single paper, whose isoform contrast and endo-lysosomal localization come from different experimental arms, which the submission records rather than papers over.

## Code and prompts

The two protocols, including their full prompt sets, are public in the repositories linked at the top of this file. Per-hypothesis search logs, screening and extraction records, and the validated submission spreadsheets are in this repository (`search-logs/`, `methods/`, `submissions/`).

---

## Licence and citation

Method description: free to read and reuse with attribution. The two underlying protocols carry their own licences (Malikian Attribution Non-Commercial Licence; see each repository).

Malikian R. MecCog Challenge APOE4 Evidence Review: combined multi-agent Cochrane-level review and peer review method. 2026–2027. GitHub: https://github.com/rtmalikian/meccog-apoe4-evidence-review · ORCID: 0009-0008-4326-4205
