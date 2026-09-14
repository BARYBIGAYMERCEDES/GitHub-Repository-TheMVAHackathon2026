# The MVA Hackathon 2026 — MVA-PRISM

## Overview

This repository contains **MVA-PRISM**, a reproducible genomic variant-prioritization workflow developed for **Track 1 — Variant Prediction** of the **Rare Disease, Real Kid: MVA Hackathon 2026**.

The objective is to prioritize plausible causal genomic variants for a real patient with Mosaic Variegated Aneuploidy (MVA) using controlled-access whole-genome sequencing data, structured clinical phenotype information, inheritance modeling, and variant-level evidence.

> **Important:** No controlled-access patient genomic files or original clinical records are included in this repository.

## Project Goals

MVA-PRISM integrates:

- Whole-genome variant quality control
- Rare-variant filtering
- Phenotype/HPO-driven prioritization
- Mendelian inheritance modeling
- Compound-heterozygous candidate detection
- Variant pathogenicity assessment
- Chromosomal-instability/MVA biological prioritization
- Evidence-based ranking of candidate causal variants
- Reproducible Track 1 submission generation

## Track 1 Submission

The current submission is:

- `BARYBIGAY_MVA-PRISM-v1_track1_submission.csv`

Supporting materials:

- `BARYBIGAY_MVA-PRISM-v1_methods_description.xlsx`
- `BARYBIGAY_MVA-PRISM-v1_track1_report.pdf`

The primary analysis prioritizes a **candidate biallelic/compound-heterozygous BUB1B model**. Phase has not been assumed unless directly established by the available data; therefore, the interpretation is presented as a candidate molecular model rather than a confirmed phased genotype.

## Repository Structure

```text
GitHub-Repository-TheMVAHackathon2026/
├── README.md
├── .gitignore
├── submission/
│   └── BARYBIGAY_MVA-PRISM-v1_track1_submission.csv
├── methods/
│   └── BARYBIGAY_MVA-PRISM-v1_methods_description.xlsx
├── reports/
│   └── BARYBIGAY_MVA-PRISM-v1_track1_report.pdf
├── src/
│   └── reproducible analysis scripts
└── config/
    └── analysis configuration files
```

## Analysis Framework

### 1. Phenotype Definition

Clinical findings are represented using Human Phenotype Ontology (HPO) terms and interpreted as a combined phenotype rather than as isolated features.

### 2. Variant QC and Filtering

The workflow evaluates candidate variants using available sequence-level quality metrics and prioritizes rare or clinically relevant variants compatible with the phenotype and disease mechanism.

### 3. Inheritance Modeling

The analysis considers:

- Autosomal recessive inheritance
- Compound heterozygosity
- Homozygous variants
- Dominant and X-linked models when relevant
- Mosaic or complex mechanisms when supported by the data

### 4. MVA-Specific Biological Prioritization

Candidates are assessed in the context of biological pathways relevant to MVA and chromosomal instability, including mitotic checkpoint control, chromosome segregation, centrosomal function, and related mechanisms.

### 5. Candidate Ranking

Candidate variants are ranked using an integrated evidence framework that considers:

- Variant quality
- Population rarity
- Predicted molecular consequence
- Clinical classification evidence
- Phenotype concordance
- Inheritance compatibility
- Disease-gene validity
- Mechanistic plausibility

## Reproducibility

The repository is intended to provide sufficient code and configuration to reproduce the analytical workflow **without redistributing controlled-access patient data**.

Authorized participants must obtain the original genomic and clinical data directly from the official MVA Hackathon dataset under its access conditions.

## Data Privacy and Security

This repository does **not** include:

- FASTQ files
- BAM/CRAM files
- Raw or complete VCF files
- Original patient clinical documents
- Any additional controlled-access source material

Participants and users of this repository are responsible for complying with the Hackathon data-use terms, IRB-related restrictions, and patient privacy requirements.

## AI-Assisted Analysis

AI-assisted methods were used as part of the analytical and documentation workflow. Relevant provider, plan/tier, and data-handling disclosures are documented in the submitted methods description in accordance with the Hackathon requirements.

## Limitations

Candidate prioritization is a research hypothesis-generation process. A ranked variant or variant pair is not equivalent to a clinically confirmed diagnosis. Confirmation may require orthogonal validation, segregation analysis, phasing, functional studies, and expert clinical interpretation.

## Citation / Attribution

If you reuse code, methods, or analytical concepts from this repository, please provide appropriate attribution.

Hackathon research outputs are intended to be shared under **CC BY 4.0** where applicable under the competition rules.

## Author

**Bary G. Bigay Mercedes, MD, MSc, MBA, IFCAP**  
Clinical Genetics and Molecular Biology  
Instituto ChromoMED  
Santo Domingo, Dominican Republic

## Competition

**Rare Disease, Real Kid: The MVA Hackathon 2026**  
Track 1 — Variant Prediction
