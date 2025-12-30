[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
Awesome Tools AI 4 Nanobody

A curated, research-oriented collection of AI tools, models, datasets, and workflows for nanobody (VHH / VNAR) discovery, design, optimization, and evaluation.

This repository is inspired by the AI4Protein 2025 landscape and refocused specifically on nanobody-centric use cases.
It is not a ranking. The taxonomy is pragmatic rather than theoretical. Omissions and imperfections are expected and welcome to be fixed via community contributions.

Contents

Scope

Nanobody-specific vs General Binder Matrix

End-to-end Nanobody Design and Optimization

Antibody and VHH/VNAR Design

Binder Design (General Protein Binders)

Structure Prediction

Affinity, Stability, and Developability Prediction

Conformation Sampling and Dynamics

Protein Language Models

Agents and Automated Research Workflows

Datasets, Benchmarks, and Databases

Practical Workflow Templates

Acknowledgement

Contributing

License

Scope

This list focuses on tools that directly support real nanobody research workflows, including:

VHH/VNAR sequence generation and CDR design

Antigen–nanobody complex structure prediction

Binder design frameworks adaptable to nanobody discovery

Affinity, ΔΔG, stability, and developability prediction

Conformational sampling for flexible or IDR-rich epitopes

AI agents for design–build–test–learn cycles

Benchmarks and datasets suitable for evaluation and comparison

Nanobody-specific vs General Binder Matrix
Tool / Framework	Category	Primary Use Case	Typical Input	Typical Output	Nanobody-specific	Typical Failure Mode
RFantiboy	Nanobody / Antibody	de novo VHH design	Target structure / epitope	VHH sequences, backbones	Yes	Unrealistic CDR geometry
Germinal	Antibody / VHH	Antibody/VHH optimization	Antibody/VHH sequences	Optimized sequences	Yes	Framework bias
IgGM	Antibody	Framework-aware design	Antibody sequences	Stabilized variants	Partial	Limited VHH diversity
MAGE	Antibody	LM-based antibody design	Sequence, epitope hints	Antibody sequences	Partial	Weak structure grounding
NanoBinder	Binder	Nanobody-like binder design	Target structure	Small binders	Partial	Not strict VHH topology
HalluDesign	General Binder	Interface design	Structure, constraints	Designed regions	No	Interface hallucination
RFdiffusion3	General Binder	de novo binder scaffolds	Target structure	Backbone + sequence	No	Overconfident binders
BindCraft	Protein Binder	de novo protein binders	Target structure	Protein binders	No	Rigid interfaces
ODesign	General Binder	Protein and binder design	Structure / sequence	Designed proteins	No	Mode collapse
BoltzGen	General Binder	Generative design	Constraints	Candidate binders	No	Low functional diversity
Graphinity	Scoring	Antigen–antibody ΔΔG	Complex structure	ΔΔG scores	Antibody-aware	Sensitive to structure quality
ProAffinity++	Scoring	PPI affinity prediction	Complex structure	Affinity ranking	No	Absolute values unreliable
ITsFlexible	Antibody	CDR flexibility	Antibody structure	Flexibility metrics	Yes	Misses slow dynamics
STAB-DDG	Stability	Mutation stability	Structure + mutation	ΔΔG stability	No	Poor for large rearrangements
End-to-end Nanobody Design and Optimization

Common pipeline-style tools:

Germinal

IgGM

RFantiboy

Chai-2

JAM-2

tFold System

Typical loop:
sequence generation → structure/complex prediction → affinity & stability scoring → developability filtering → iteration with experimental feedback

Antibody and VHH/VNAR Design
VHH-focused tools

RFantiboy

Germinal

EvolveX

mBER

ODesign

BoltzGen

FoldCraft

Nanodesigner

GeoFlow-V2 / GeoFlow-V3

nanoFOLD

CDR design and affinity maturation

HalluDesign

UniMoMo

MFDesign

Binder Design (General Protein Binders)

General binder tools frequently used upstream or alongside nanobody programs:

RFdiffusion3 / RFdiffusion2

HalluDesign

Protein Hunter

ODesign

BoltzGen / BoltzDesign1

OriginFlow

Neo-1

Protein binder–focused frameworks:

BindCraft

PXDesign

BinderFlow

UniMoMo

Prot42

BindEnergyCraft

Mosaic (escalante-bio)

Structure Prediction
Protein and complex prediction

ESM3

RosettaFold3

OpenFold3

Boltz-1x

CryoBoltz

AF3Complex

D-I-TASSER

IntFold

TDFold

MultiFOLD2

Antibody and loop context

AutoLoop

AbEpiTope

Cyclic peptides (epitope probing, alternatives)

CyclicBoltz1

AfCycDesign

HighFold3

MeDCycFold

Affinity, Stability, and Developability Prediction

Graphinity

ProAffinity++

PCANN

MPBind

BindFlow

AlphaPPIMI

ProteomeLM

SWING

SpatPPI

Stability and mutation effects:

STAB-DDG

ProStab

DVE-stability

ESMDance

Structure quality and flexibility:

ITsFlexible

AF3Score

FoldScript

ContrastQA

actifpTM

ELEN

Conformation Sampling and Dynamics

BioEmu

ESMDiff

AlphaFlex

PTraj-Diff

CryoPhold

STARLING (IDP-focused)

BAMBOO (ML force field)

MD-LLM-1

Protein Language Models
PLM

ProGen3

PoET-2

μFormer

DePLM

xTrimoPGLM

ProtBFN / AbBFN

ProteinReasoner

MSA Pairformer

ProteinGPT

Prot42

PTM-Mamba

InterPLM

GLM (target biology context)

AlphaGenome

Evo2

LucaOne

BioReason

CodonTransformer

OmniReg-GPT

Agents and Automated Research Workflows

Virtual Lab

CRISPR-GPT

BioMni

STELLA

DrBioRight

PrimeGen

AgentD

Biomedical AI-Q

NVIDIA AI-Q

BiomedGPT

MedGemma

Datasets, Benchmarks, and Databases

FoldBench

VenusPod

VenusMutHub

ALL-conformations

MolGlueDB

Search and alignment:

MMseqs2_GPU

FAMSA2

Foldseek-Multimer

PreTrek

Practical Workflow Templates
Template A: VHH discovery

Sequence generation (RFantiboy, BoltzGen, AbBFN)

Structure / complex prediction (ESM3, RosettaFold3)

Affinity scoring (Graphinity, ProAffinity++)

Stability filtering (STAB-DDG, ProStab)

Sampling validation (BioEmu, ESMDiff)

Template B: CDR-focused affinity maturation

CDR proposal (HalluDesign, UniMoMo)

Re-modeling and rescoring

Stability guardrails

Active learning with wet-lab feedback

Acknowledgement

This repository is inspired by and builds upon the AI4Protein community’s continuous effort in tracking and interpreting AI-for-protein research.

“死磕自己，愉悦大家，专注于 AI 蛋白相关的论文解读与学术速运。”

Bilibili video replays: search for the account name AI4Protein.

Contributing

Contributions are welcome via pull requests or issues.

Suggested metadata for new entries:

Tool name

Target task

Typical input and output

Typical failure mode

Reference (paper, repository, or documentation)

License

This work is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

You are free to share and adapt the material for any purpose, including commercial use, provided appropriate credit is given.

License text:
https://creativecommons.org/licenses/by/4.0/
