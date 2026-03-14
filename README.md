# Germline Variant Calling Pipeline

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS-lightgrey)
![License](https://img.shields.io/badge/license-MIT-blue)

## Overview

An end-to-end germline short variant calling pipeline following
[GATK Best Practices](https://gatk.broadinstitute.org/hc/en-us/articles/360035535932).

Applied to publicly available whole genome sequencing data from
**NA12878 (HG001)** — the Genome in a Bottle benchmark sample —
subsetted to **chromosome 20** for computational efficiency.

**Pipeline:** FastQC → Trimmomatic → BWA-MEM → GATK HaplotypeCaller
→ VariantFiltration

---

## Project Status

- [x] Environment setup
- [x] Data downloaded
- [ ] Quality control (FastQC + MultiQC)
- [ ] Adapter trimming (Trimmomatic)
- [ ] Alignment (BWA-MEM)
- [ ] Duplicate marking (GATK MarkDuplicates)
- [ ] Variant calling (GATK HaplotypeCaller)
- [ ] Variant filtering (GATK VariantFiltration)
- [ ] Results notebook

---

## Repository Structure
```
germline-variant-calling-pipeline/
│
├── README.md
├── environment.yml
│
├── data/              # Raw data — not tracked by git
├── scripts/           # One numbered shell script per pipeline step
├── results/           # Pipeline outputs — not tracked by git
├── notebooks/         # Jupyter notebook for results exploration
└── docs/              # Lab notebook and diagrams
```

---

## Dataset

| Field | Detail |
|---|---|
| Sample | NA12878 (HG001) |
| Accession | ERR194147 (ENA / NCBI SRA) |
| Sequencing platform | Illumina HiSeq 2000 |
| Read length | 100bp paired-end |
| Coverage | ~30x whole genome |
| Reference genome | GRCh38 (hg38), chromosome 20 only |

> **Why chromosome 20 only?** The full dataset is ~90GB. Restricting
> to chr20 reduces working data to ~1–2GB while fully demonstrating
> every step of the pipeline. All tools and parameters are identical
> to a full-genome run.

---

## Tools & Versions

| Tool | Version | Purpose |
|---|---|---|
| FastQC | 0.12.1 | Raw read quality control |
| MultiQC | 1.21 | QC report aggregation |
| Trimmomatic | 0.39 | Adapter trimming |
| BWA-MEM | 0.7.17 | Read alignment |
| samtools | 1.19 | BAM sorting and indexing |
| GATK | 4.5.0 | Duplicate marking and variant calling |
| Python | 3.11 | Results notebook |

Full software environment: [`environment.yml`](environment.yml)

---

## Installation

**1. Clone this repository**
```bash
git clone git@github.com:YOURUSERNAME/germline-variant-calling-pipeline.git
cd germline-variant-calling-pipeline
```

**2. Recreate the conda environment**
```bash
conda env create -f environment.yml
conda activate variant-calling
```

---

## Results

> Pipeline in progress — results will be added upon completion.

---

## References

- [GATK Best Practices — Germline SNPs & Indels](https://gatk.broadinstitute.org)
- [Genome in a Bottle Consortium (NIST)](https://www.nist.gov/programs-projects/genome-bottle)
- [NA12878 accession ERR194147 (ENA)](https://www.ebi.ac.uk/ena/browser/view/ERR194147)# germline-variant-calling-pipeline
End-to-end germline variant calling pipeline using GATK best practices on NA12878 WGS data (chr20)
