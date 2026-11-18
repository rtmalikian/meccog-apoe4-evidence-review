# H2 Verification — Screener B (independent second pass)

**Hypothesis H2:** "In some types of non-Alzheimer's, non-aged human brain cells, for example astrocytes, APOE4 causes impaired ARF6-related recycling of receptors between the cell surface and the endosome, compared with APOE3."

**Verification criterion applied:** the paper is an experimental study that directly tests APOE4 vs APOE3/APOE2, or APOE4 manipulation, on ARF6-pathway recycling of receptors between the cell surface and the endosome — i.e. a receptor recycling / endosomal recycling assay, ARF6 activity or manipulation in an APOE-isoform context, or recycling of a specific receptor (ABCA1, ApoER2, LRP1, LDLR, insulin receptor, AMPA receptors) where the recycling step itself is measured. Model systems count. Reviews/meta-analyses, GWAS-only, clinical/epidemiological correlation-only, editorials, protocols and keyword-only matches are excluded. Verification was made from the abstracts in `work/searches2/H2.json` and `work/searches2/H2r2.json` only. Note: this criterion is stricter than Screener A's on one point — A also admitted a receptor's surface-vs-endosome distribution (endosomal trapping / surface loss) as a proxy for failed recycling even where no recycling step was assayed. Papers that pass A's broader rule but not the recycling-step-itself rule are held out below as Disputed, not confirmed.

**Starting reference check (prominent):** Rawat V, et al., J Neurosci 2019, PMID 31641056, DOI 10.1523/jneurosci.1400-19.2019, "ApoE4 Alters ABCA1 Membrane Trafficking in Astrocytes" — **VERIFIED: in the pool (present in the deduped union) and CONFIRMED as eligible, ranked #1.** Its abstract states that ApoE4, compared with ApoE3, promoted greater expression of ARF6, trapping ABCA1 in late endosomes and impairing its recycling to the cell membrane. It is the only record in the pool that names ARF6 (verified by full-pool text search), and it is the single most direct test of H2.

## Counts

- Screened: **253** (deduped union of Run 1, 200 records, and Run 2, 130 records)
- A-shortlisted: **7**
- Confirmed: **4**
- Disputed: **3** (all from A's shortlist; held out, not counted as confirmed)
- Borderline-excluded: **9** listed below (A excluded all of them; B agrees with each exclusion, for the reasons given)
- Added by B beyond A's list: **0** — an independent scan of the full deduped pool (all records whose title or abstract mentions recycling, trafficking, endosomes or surface expression, plus all non-review records mentioning APOE4 with a trafficking/endosomal term) found no paper meeting the criterion that A had excluded. A's "recycling with no APOE comparison" and "experimental but off-target" categories were re-read and their exclusions upheld.

## Confirmed

Ranked by directness to H2, most direct first.

1. DOI: 10.1523/jneurosci.1400-19.2019 — 2019 — Rawat V — "ApoE4 Alters ABCA1 Membrane Trafficking in Astrocytes." (Starting reference. The only ARF6 paper in the pool: ApoE4 vs ApoE3 increases ARF6 expression, traps ABCA1 in late endosomes and impairs ABCA1 recycling to the cell membrane in astrocytes, with reduced ABCA1-mediated cholesterol efflux; human APOE ε4/ε4 vs ε3/ε3 CSF comparison included.)
2. DOI: 10.7554/elife.40048 — 2018 — Xian X — "Reversal of ApoE4-induced recycling block as a novel prevention approach for Alzheimer's disease." (Direct receptor-recycling endpoint: pharmacological and genetic NHE6 inhibition completely reverses the ApoE4-induced recycling block of Apoer2/Lrp8 and of the co-endocytosed AMPA- and NMDA-type glutamate receptors, restoring Reelin-mediated synaptic modulation.)
3. DOI: 10.1073/pnas.0914984107 — 2010 — Chen Y — "ApoE4 reduces glutamate receptor function and synaptic plasticity by selectively impairing ApoE receptor recycling." (ApoE4 selectively impairs ApoE receptor recycling: reduced neuronal surface expression of Apoer2, NMDA and AMPA receptors by sequestration in intracellular compartments, in human ApoE4 knockin mice; the recycling impairment is the paper's stated mechanism.)
4. DOI: 10.1016/j.cell.2024.10.027 — 2025 — Guo JL — "Decreased lipidated ApoE-receptor interactions confer protection against pathogenicity of ApoE and its lipid cargoes in lysosomes." (LDLR recycling defects measured in human neurons with lipidated ApoE3/E4, avoided by lipidated ApoE2 and by the Christchurch mutant. Caveat: the recycling contrast is chiefly E3/E4 vs E2 — the abstract reports no E4-vs-E3 difference in LDLR recycling itself. Confirmed because the eligibility rule admits an APOE4-vs-APOE2 test and the recycling step itself was measured; ranked last for this reason.)

## Disputed

Each of the following was included by A under A's broader surface-vs-endosome-distribution proxy. On B's re-reading of the abstracts, none assays the recycling step itself: each measures endosomal trapping and/or loss of surface expression, from which failed recycling is inferred. They are genuinely arguable both ways and are therefore held out as disputed rather than confirmed or excluded.

1. **DOI: 10.1073/pnas.1801612115 — 2018 — Prasad H — "Amyloid clearance defect in ApoE4 astrocytes is reversed by epigenetic correction of endosomal pH."**
   Reason: in ApoE4 vs ApoE3 astrocytes, aberrant endosomal acidification (via NHE6 down-regulation) traps LRP1 within intracellular compartments, causing loss of LRP1 surface expression and defective Aβ clearance; HDAC inhibitors restore NHE6, LRP1 trafficking and clearance. The endpoints are trapping, surface loss and clearance — no recycling assay is reported in the abstract. A itself noted "a recycling assay per se is not the headline endpoint."

2. **DOI: 10.1016/j.neuron.2017.09.003 — 2017 — Zhao N — "Apolipoprotein E4 Impairs Neuronal Insulin Signaling by Trapping Insulin Receptor in the Endosomes."**
   Reason: apoE4 interacts with the insulin receptor and impairs its trafficking by trapping it in endosomes in apoE-targeted replacement mice and primary neurons, impairing insulin signalling. Endosomal trapping is measured; recycling of the receptor back to the surface is inferred from the trapping, not assayed.

3. **DOI: 10.3233/jad-230514 — 2024 — Safieh M — "The Role of Impaired Receptor Trafficking in Mediating the Pathological Effects of APOE4 in Alzheimer's Disease."**
   Reason: in primary neurons from APOE3- vs APOE4-targeted replacement mice, cell-surface biotinylation and compartmentalisation show lower surface levels of ApoER2, LRP1, insulin receptor and VEGFR in APOE4 neurons, with early-endosome accumulation for most receptors. Surface-vs-intracellular distribution is measured across four receptors, but recycling kinetics are not assayed.

## Borderline-excluded

A excluded each of these; B re-read the abstracts and agrees, for the reasons given. None is counted as confirmed or disputed.

1. **DOI: 10.1073/pnas.0508693102 — 2005 — Ye H (et al.) — "Apolipoprotein (apo) E4 enhances amyloid beta peptide production in cultured neuronal cells."** Recycling is genuinely measured and apoE4 exceeds apoE3 — but the cargo is APP, not a receptor, and the direction is opposite to H2 (apoE4 *stimulates* APP recycling). Off-target on both cargo and direction.
2. **DOI: 10.1186/s13024-025-00802-7 — 2025 — Wang (et al.) — "Cellular senescence induced by cholesterol accumulation is mediated by lysosomal ABCA1 in APOE4 and AD."** ABCA1 endolysosomal trafficking / lysosomal trapping is studied in APOE4 models, but the endpoint is cellular senescence, no surface-recycling assay is reported, and the abstract states no APOE4-vs-APOE3 recycling comparison. Weaker than the disputed trapping papers, which each measure surface loss of a named receptor in a direct isoform comparison.
3. **DOI: 10.1016/j.celrep.2020.108224 — 2020 — Narayan P (et al.) — "PICALM Rescues Endocytic Defects Caused by the Alzheimer's Disease Risk Factor APOE4."** Direct APOE4-vs-isogenic-APOE3 comparison in human iPSC-derived astrocytes, but the measured step is endocytosis (uptake), not recycling back to the surface. Endocytosis-only; correctly excluded.
4. **DOI: 10.1126/scisignal.aaa6674 — 2015 — Lane-Donovan C (et al.) — "Reelin protects against amyloid β toxicity in vivo."** The ApoE4 impairment of Apoer2/Vldlr recycling is cited from the group's prior work ("We have previously shown…"); this paper's own experiments test Reelin knockout and Aβ toxicity in vivo, with synaptic and memory endpoints. No recycling measurement in this paper.
5. **DOI: 10.7554/elife.72034 — 2021 — Pohlkamp T (et al.) — "NHE6 depletion corrects ApoE4-mediated synaptic impairments and reduces amyloid plaque load."** NHE6 loss reverses the ApoE4 endolysosomal trafficking defect at the level of synaptic homeostasis and amyloid load, but no receptor-recycling endpoint is reported in the abstract; the recycling block itself is background from prior work.
6. **DOI: 10.1002/advs.202510270 — 2025 — (uric acid study) — "Uric Acid Functions as an Endogenous Modulator of Microglial Function and Amyloid Clearance in Alzheimer's Disease."** Uric acid restores recycling of the Aβ receptors CD36 and TREM2 in microglia of 5×FAD mice — a genuine receptor-recycling measurement, but with no APOE isoform comparison and no APOE4 manipulation. Correctly excluded.
7. **DOI: 10.3390/biom14070799 — 2024 — Fuentealba LM (et al.) — "OCRL1 Deficiency Affects the Intracellular Traffic of ApoER2 and Impairs Reelin-Induced Responses."** ApoER2 endosomal recycling is measured, but the manipulation is OCRL1 deficiency (Lowe syndrome); no APOE isoform comparison. Correctly excluded.
8. **DOI: 10.1194/jlr.m014365 — 2011 — Fan J (et al.) — "An ABCA1-independent pathway for recycling a poorly lipidated 8.1 nm apolipoprotein E particle from glia."** The recycled cargo is the apoE particle itself (via LDLR), with no APOE isoform comparison. Correctly excluded.
9. **DOI: 10.1371/journal.pone.0029385 — 2012 — Laatsch A (et al.) — "Low density lipoprotein receptor-related protein 1 dependent endosomal trapping and recycling of apolipoprotein E."** LRP1-dependent recycling of apoE itself in human hepatoma cells; no APOE isoform comparison, non-brain cells, and the recycled cargo is apoE rather than a receptor. Correctly excluded.

## DOI corrections

None. All seven DOIs on A's shortlist were checked against their Europe PMC records in the search JSONs: in every case the DOI, PMID and title are mutually consistent (Rawat 2019, PMID 31641056; Xian 2018, PMID 30375977; Chen 2010, PMID 20547867; Guo 2025, PMID 39532095; Prasad 2018, PMID 29946028; Zhao 2017, PMID 28957663; Safieh 2024, PMID 38217595). No DOI appeared malformed or mismatched to its title, and every confirmed and disputed paper has a DOI in its record, so no "N/A" entries were needed. No DOI was guessed or supplied from outside the records.
