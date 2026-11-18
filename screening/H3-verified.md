# H3 Inclusion Verification — Screener B (independent second screen)

**Hypothesis H3 (verbatim):** "APOE4 increases tau pathology, through actions that include enhancing tau phosphorylation, release, propagation, and neuroinflammation. Increased tau pathology then drives disease risk."

**Scope verified:** all 16 papers included by Screener A across Run 1 (`screening/H3-shortlist.md`, 3 papers) and Run 2 (`screening/H3-shortlist-r2.md`, 13 papers).

**Verification rule (applied to the abstract of each paper, as recorded in `searches/H3.json` / `searches/H3r2.json`):** the paper must be an experimental study that directly tests APOE4 — against APOE3/APOE2, or via an APOE4 manipulation — with an effect on tau phosphorylation, tau release, tau propagation/spread, tau pathology burden, or tau-related neuroinflammation, and with tau actually measured.

## Counts

- Verified: 16
- Confirmed: 11
- Disputed: 5

## Confirmed (11)

Each of these is an experimental study whose abstract reports a direct APOE4 isoform comparison or APOE4 manipulation with a tau outcome (phosphorylation, pathology burden, or tauopathy-linked neuroinflammation) measured.

| # | DOI | Year | First author | Title |
|---|-----|------|--------------|-------|
| 1 | 10.1038/nature24016 | 2017 | Shi Y | ApoE4 markedly exacerbates tau-mediated neurodegeneration in a mouse model of tauopathy. |
| 2 | 10.1038/s41586-024-07185-7 | 2024 | Haney MS | APOE4/4 is linked to damaging lipid droplets in Alzheimer's disease microglia. |
| 3 | 10.1016/j.neuron.2021.03.024 | 2021 | Wang C | Selective removal of astrocytic APOE4 strongly protects against tau-mediated neurodegeneration and decreases synaptic phagocytosis by microglia. |
| 4 | 10.1038/s41591-018-0004-z | 2018 | Wang C | Gain of toxic apolipoprotein E4 effects in human iPSC-derived neurons is ameliorated by a small-molecule structure corrector. |
| 5 | 10.1523/jneurosci.4315-03.2004 | 2004 | Brecht WJ | Neuron-specific apolipoprotein e4 proteolysis is associated with increased tau phosphorylation in brains of transgenic mice. |
| 6 | 10.1016/s0002-9440(10)64963-2 | 2000 | Tesseur I | Expression of human apolipoprotein E4 in neurons causes hyperphosphorylation of protein tau in the brains of transgenic mice. |
| 7 | 10.1038/s41467-020-19264-0 | 2020 | Zhao J | APOE4 exacerbates synapse loss and neurodegeneration in Alzheimer's disease patient iPSC-derived cerebral organoids. |
| 8 | 10.1126/science.add1236 | 2023 | Seo DO | ApoE isoform- and microbiota-dependent progression of neurodegeneration in a mouse model of tauopathy. |
| 9 | 10.1038/s41593-021-00851-3 | 2021 | Zalocusky KA | Neuronal ApoE upregulates MHC-I expression to drive selective neurodegeneration in Alzheimer's disease. |
| 10 | 10.1073/pnas.151254698 | 2001 | Huang Y | Apolipoprotein E fragments present in Alzheimer's disease brains induce neurofibrillary tangle-like intracellular inclusions in neurons. |
| 11 | 10.1073/pnas.1434398100 | 2003 | Harris FM | Carboxyl-terminal-truncated apolipoprotein E4 causes Alzheimer's disease-like neurodegeneration and behavioral deficits in transgenic mice. |

## Disputed (5)

Flagged because, on the abstract as recorded, the paper does not clearly meet the verification rule. Each entry states the specific gap; adjudication against the full text is recommended before final inclusion.

### 1. Microglia drive APOE-dependent neurodegeneration in a tauopathy mouse model.
- **DOI:** 10.1084/jem.20190980 · **Year:** 2019 · **First author:** Shi Y
- **Reason:** The abstract describes APOE's role generically — microglia drive neurodegeneration and phospho-tau pathology progression, and APOE regulates this mainly via microglial activation, with a minor microglia-independent effect on ptau and insoluble tau. No APOE isoform is named anywhere in the abstract: there is no APOE4-vs-APOE3/APOE2 comparison and no APOE4-specific manipulation described, so the APOE4-specific test required by the rule cannot be verified from the abstract.

### 2. APOE4 impairs the microglial response in Alzheimer's disease by inducing TGFβ-mediated checkpoints.
- **DOI:** 10.1038/s41590-023-01627-6 · **Year:** 2023 · **First author:** Yin Z
- **Reason:** No tau outcome is reported in the abstract. Microglial APOE4 deletion in P301S tau transgenic mice is reported to restore the neurodegenerative-microglia (MGnD) phenotype "associated with neuroprotection," but no change in tau phosphorylation, tau burden, or tau pathology is stated; the only pathology reduction explicitly claimed is in APP/PS1 (amyloid) mice. Tau being actually measured, as the rule requires, is not evident from the abstract.

### 3. Apolipoprotein E4 causes age- and Tau-dependent impairment of GABAergic interneurons, leading to learning and memory deficits in mice.
- **DOI:** 10.1523/jneurosci.4040-10.2010 · **Year:** 2010 · **First author:** Andrews-Zwilling Y
- **Reason:** The tested outcomes are GABAergic interneuron loss and learning/memory deficits. Tau enters the design as a manipulated mediator — eliminating endogenous tau prevented the interneuron loss — rather than as an APOE4-driven outcome: the abstract reports that tauopathy "occurred earliest" in hilar interneurons of apoE4-fragment mice but gives no APOE4-vs-APOE3/APOE2 comparison of tau phosphorylation or tau pathology burden, so a direct test of APOE4's effect on tau is not demonstrated in the abstract.

### 4. Lipid- and receptor-binding regions of apolipoprotein E4 fragments act in concert to cause mitochondrial dysfunction and neurotoxicity.
- **DOI:** 10.1073/pnas.0508254102 · **Year:** 2005 · **First author:** Chang S
- **Reason:** The study is a structure–function analysis of apoE4 fragments in transfected Neuro-2a cells whose tested outcomes are mitochondrial dysfunction and neurotoxicity. Phosphorylated tau appears only incidentally — apoE4(1–272) "formed filamentous inclusions containing phosphorylated tau in some cells" — and no APOE3/APOE2 comparator is reported in the abstract. Tau phosphorylation is observed, not directly tested as an APOE4 effect.

### 5. Isoform-specific interactions of apolipoprotein E with microtubule-associated protein tau: implications for Alzheimer disease.
- **DOI:** 10.1073/pnas.91.23.11183 · **Year:** 1994 · **First author:** Strittmatter WJ
- **Reason:** This is an in vitro binding study: tau bound apoE3 but not apoE4, and phosphorylated tau bound neither isoform. None of the outcomes named in the rule is measured — no effect of APOE4 on tau phosphorylation, release, propagation/spread, pathology burden, or tau-related neuroinflammation is tested; the paper characterises a physical apoE–tau interaction and infers a mechanism. It does not experimentally test an APOE4 effect on tau pathology.
