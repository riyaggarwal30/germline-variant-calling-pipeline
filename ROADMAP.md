# Project Roadmap — Germline Variant Calling Pipeline

This file tracks weekly progress on the project.
Update checkboxes as you complete each task.

---

## Week 1 — Foundations & Setup
- [ ] Read Illumina NGS introduction PDF
- [ ] Read GATK best practices overview page
- [ ] Read Genome in a Bottle / NA12878 overview
- [ ] Install Miniconda
- [ ] Add bioconda and conda-forge channels
- [ ] Create `variant-calling` conda environment
- [ ] Install FastQC, MultiQC
- [ ] Install Trimmomatic
- [ ] Install BWA, samtools
- [ ] Install GATK4
- [ ] Install SRA Toolkit
- [ ] Verify all tools with `--version`
- [ ] Create GitHub repo
- [ ] Clone repo locally
- [ ] Create folder structure (`data/`, `scripts/`, `results/`, `notebooks/`, `docs/`)
- [ ] Configure `.gitignore`
- [ ] Export `environment.yml`
- [ ] Write Day 1 README
- [ ] Download NA12878 reads (ERR194147)
- [ ] Download chr20 reference (GRCh38)
- [ ] Index reference with BWA, samtools, GATK
- [ ] Write first lab notebook entry
- [ ] Push everything to GitHub

---

## Week 2 — Quality Control
- [ ] Run FastQC on raw R1 and R2 reads
- [ ] Run MultiQC to aggregate reports
- [ ] Interpret FastQC HTML report
- [ ] Check per-base quality scores
- [ ] Check adapter content
- [ ] Check duplication levels
- [ ] Write `scripts/01_quality_control.sh`
- [ ] Update README results table with raw read count
- [ ] Write lab notebook entry for Week 2
- [ ] Commit and push

---

## Week 3 — Trimming & Alignment
- [ ] Run Trimmomatic on raw reads
- [ ] Verify paired output files exist
- [ ] Run FastQC on trimmed reads to confirm improvement
- [ ] Write `scripts/02_trimming.sh`
- [ ] Index reference genome (if not done in Week 1)
- [ ] Run BWA-MEM alignment
- [ ] Sort BAM with samtools
- [ ] Index BAM with samtools
- [ ] Run samtools flagstat — note alignment rate
- [ ] Write `scripts/03_alignment.sh`
- [ ] Update README results table with alignment rate
- [ ] Write lab notebook entry for Week 3
- [ ] Commit and push

---

## Week 4 — Variant Calling
- [ ] Run GATK MarkDuplicates
- [ ] Check duplication rate in metrics file
- [ ] Run GATK HaplotypeCaller
- [ ] Inspect raw VCF output
- [ ] Count raw variants (SNPs + indels)
- [ ] Write `scripts/04_variant_calling.sh`
- [ ] Update README results table with raw variant count
- [ ] Write lab notebook entry for Week 4
- [ ] Commit and push

---

## Week 5 — Filtering & Results
- [ ] Run GATK VariantFiltration
- [ ] Count variants passing filters
- [ ] Separate SNP and indel counts
- [ ] Calculate Ti/Tv ratio
- [ ] Write `scripts/05_filter.sh`
- [ ] Update README results table with final numbers
- [ ] Write lab notebook entry for Week 5
- [ ] Commit and push

---

## Week 6 — Notebook & Final Polish
- [ ] Set up Jupyter notebook
- [ ] Parse VCF with cyvcf2
- [ ] Plot SNP vs indel counts
- [ ] Plot quality score distribution
- [ ] Calculate and interpret Ti/Tv ratio
- [ ] Write interpretation paragraph in notebook
- [ ] Fill in all README results table values
- [ ] Write known limitations section in README
- [ ] Add parameter justification section to README
- [ ] Final read-through of entire README
- [ ] Make repo look clean (clear commit messages, tidy structure)
- [ ] Final commit and push

---

## Progress Tracker

| Week | Topic | Status |
|---|---|---|
| Week 1 | Foundations & Setup | 🔄 In progress |
| Week 2 | Quality Control | ⬜ Not started |
| Week 3 | Trimming & Alignment | ⬜ Not started |
| Week 4 | Variant Calling | ⬜ Not started |
| Week 5 | Filtering & Results | ⬜ Not started |
| Week 6 | Notebook & Final Polish | ⬜ Not started |

**Legend:** ✅ Done · 🔄 In progress · ⬜ Not started
> Full weekly roadmap and task checklist: [ROADMAP.md](ROADMAP.md)
```

---

## Step 2 — Commit it

Scroll down on GitHub, write the commit message:
```
Add project roadmap with weekly checklist
