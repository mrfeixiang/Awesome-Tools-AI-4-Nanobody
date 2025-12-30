# Nanobody-specific vs General Binder Matrix

This matrix is intentionally conservative. It is designed to help wet-lab and hybrid users select tools while avoiding over-trust in single-model outputs.

| Tool / Framework | Category | Primary Use Case | Typical Input | Typical Output | Nanobody-specific | Typical Failure Mode |
|---|---|---|---|---|---|---|
| RFantiboy | Nanobody / Antibody | de novo VHH design | Target structure or epitope | VHH sequences, backbones | Yes | Unrealistic CDR geometry |
| Germinal | Antibody / VHH | Antibody/VHH optimization | Antibody/VHH sequences | Optimized sequences | Yes | Framework bias |
| IgGM | Antibody | Framework-aware design | Antibody sequences | Stabilized variants | Partial | Limited VHH diversity |
| MAGE | Antibody | LM-based antibody design | Sequence, epitope hints | Antibody sequences | Partial | Weak structure grounding |
| NanoBinder | Binder | Nanobody-inspired binders | Target structure | Small binders | Partial | Not strict VHH topology |
| HalluDesign | General Binder | Interface design | Structure, constraints | Designed regions or binders | No | Interface hallucination |
| RFdiffusion3 | General Binder | de novo binder scaffolds | Target structure | Backbone + sequence | No | Overconfident binders without validation |
| BindCraft | Protein Binder | de novo protein binders | Target structure | Protein binders | No | Rigid interfaces on flexible epitopes |
| ODesign | General Binder | Protein and binder design | Structure or sequence | Designed proteins | No | Mode collapse toward common folds |
| BoltzGen | General Binder | Generative protein design | Constraints | Candidate binders | No | Low functional diversity |
| Graphinity | Scoring | Antigen–antibody ΔΔG | Complex structure | ΔΔG scores | Antibody-aware | Sensitive to structure quality |
| ProAffinity++ | Scoring | PPI affinity prediction | Complex structure | Affinity ranking | No | Absolute values unreliable |
| ITsFlexible | Antibody | CDR flexibility | Antibody structure | Flexibility metrics | Yes | Misses slow-timescale dynamics |
| STAB-DDG | Stability | Mutation stability | Structure + mutation | ΔΔG stability | No | Poor for large rearrangements |

