# MecCog Challenge — APOE4 Evidence Review: Combined Method

**Team:** Malikian Evidence Review (Raphael Malikian, solo entrant and team leader)
**Challenge:** [MecCog Challenge](https://huggingface.co/spaces/MecCog/meccog-challenge) — Papers and Findings, Step 1: connect five hypotheses about APOE4 and Alzheimer's disease risk to experimental evidence in published papers.
**Hypotheses covered:** H1 (APOE4 → ABCA1), H2 (APOE4 → amyloid β), H3 (APOE4 → tau), H4 (APOE4 → lipid accumulation and cell stress), H5 (APOE4 → synaptic and neuronal function).

This repository is the public method record for the entry. The method combines two open protocols by the same author, used together:

1. **Production pipeline** — [Multi-Agent Cochrane-Level Review Process (Robust Standard v2)](https://github.com/rtmalikian/multi-agent-cochrane-level-review-process): protocol-first searching, dual independent screening and extraction, adjudication by re-reading, and full reporting of agreement and discrepancy rates.
2. **Quality gate** — [Multi-Agent Peer Review System for Clinical AI, Medical Research and Health Technology Papers](https://github.com/rtmalikian/multi-agent-peer-review-system-clinical-ai-medical-research): persona-based reviewers and looped editorial gates, ending in a final integrity gate (Gate 6) that verifies every citation and quote against its source before anything is submitted.

Per-hypothesis method files (`methods/H1.md` … `methods/H5.md`), search logs (`search-logs/`), and the validated submission spreadsheets (`submissions/`) are committed here as each hypothesis is worked, so the record of what was actually done sits next to this description of the method.

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

PubMed and Europe PMC, searched per hypothesis with strings built from the hypothesis's own mechanism terms (APOE4 / apolipoprotein E4 plus the pathway terms: ABCA1 and lipid transport for H1; amyloid beta production and clearance for H2; tau phosphorylation and propagation for H3; lipid accumulation, lipid turnover and lysosomal function in astrocytes, microglia and neurons for H4; calcium handling and synaptic gene expression for H5), limited to experimental studies. The reference list of the Moult and Darden preprint, "Critical Assessment of Disease Mechanisms: APOE4 and Alzheimer's Disease" (2025), was citation-chased for each hypothesis. The exact string, date, source, and hit count for every search — including searches that returned nothing usable — are recorded per hypothesis in `search-logs/`.

## 4. How full text was obtained

Open-access publisher versions and PubMed Central first, then the DOI landing page. Where only the abstract was reachable, a finding drawn from it is located as "Abstract" in the submission and its directness is scored on that basis. Papers with no reachable text contribute no rows; they are counted in the per-hypothesis search log as not retrieved rather than silently dropped.

## 5. What a human checked

The Gate 6 integrity pass (an agent pass under the peer review protocol) verified every verbatim quote against the source text and every DOI against its record. The human author personally re-read every quote the integrity pass flagged, re-read a sample of the unflagged rows for each hypothesis, adjudicated every screening and extraction disagreement the agents could not settle by re-reading, and signed off each spreadsheet before it was submitted.

## 6. Anything else

Directness (F2) is scored using the challenge's own document, John Moult's *Directness of Evidence* (v02), including its ABCA1 worked examples. Strength scores (S1–S5) were assigned in two independent agent passes; disagreements were settled by re-reading the paper. Cross-hypothesis links (X1–X2) are recorded where a paper's finding bears directly on a second hypothesis, not merely where topics are adjacent. Known weaknesses: a single human author; agent extraction can misread context in dense results sections, which the dual-extraction and verbatim-quote requirements are there to catch; and the evidence base for some hypothesis sub-claims (notably barrier-specific ABCA1 effects in H1) is thin, which the submissions state rather than paper over.

## Code and prompts

The two protocols, including their full prompt sets, are public in the repositories linked at the top of this file. Per-hypothesis search logs, screening and extraction records, and the validated submission spreadsheets are in this repository (`search-logs/`, `methods/`, `submissions/`).

---

## Licence and citation

Method description: free to read and reuse with attribution. The two underlying protocols carry their own licences (Malikian Attribution Non-Commercial Licence; see each repository).

Malikian R. MecCog Challenge APOE4 Evidence Review: combined multi-agent Cochrane-level review and peer review method. 2026–2027. GitHub: https://github.com/rtmalikian/meccog-apoe4-evidence-review · ORCID: 0009-0008-4326-4205
