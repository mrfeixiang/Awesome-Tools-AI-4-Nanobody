# Awesome Tools AI 4 Nanobody

A curated, research-oriented collection of AI tools, models, datasets, and workflows for nanobody (VHH/VNAR) discovery, design, optimization, and evaluation.

This documentation site is a structured version of the repository’s README. It is not a ranking. The taxonomy is practical and open to revisions.

## Start here

- Nanobody-specific vs General Binder Matrix: [matrix](matrix.md)
- Tool categories:
  - [Nanobody design](tools/nanobody-design.md)
  - [Binder design](tools/binder-design.md)
  - [Structure prediction](tools/structure-prediction.md)
  - [Affinity, stability, developability](tools/scoring-stability.md)
  - [Sampling and dynamics](tools/sampling-dynamics.md)
  - [Protein language models](tools/language-models.md)
  - [Agents](tools/agents.md)
  - [Datasets and benchmarks](tools/datasets-benchmarks.md)

## Practical workflow templates

### Template A: VHH discovery

1) Sequence generation (RFantiboy, BoltzGen, AbBFN)  
2) Structure or complex prediction (ESM3, RosettaFold3)  
3) Affinity scoring (Graphinity, ProAffinity++)  
4) Stability filtering (STAB-DDG, ProStab)  
5) Sampling validation (BioEmu, ESMDiff)

### Template B: CDR-focused affinity maturation

1) CDR proposal (HalluDesign, UniMoMo)  
2) Re-modeling and rescoring  
3) Stability guardrails  
4) Iterate with wet-lab feedback (active learning)

## Repository pages

- [Acknowledgement](about/acknowledgement.md)
- [Contributing](about/contributing.md)
- [License](about/license.md)

