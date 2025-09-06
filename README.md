# Nationwide Multicentre Nanopore 16S rRNA Profiling Task
Overview

This evaluation task is based on a nationwide study coordinated by Genomic Medicine Sweden, assessing Oxford Nanopore long-read sequencing for full-length 16S rRNA bacterial species identification. The workflow covers DNA extraction, library preparation, sequencing, and bioinformatic analysis with both commercial and open-source pipelines.

The task evaluates sequencing reproducibility, species-level identification, and pipeline performance across multiple laboratories.

Dataset

Study: Nationwide multicentre evaluation of Nanopore sequencing for 16S rRNA species identification

Accession: SRA project SUB14925052 (mock panels + QCMD external quality assessment samples)

Samples:

GMS mock panel (13 monomicrobial/polymicrobial bacterial strains, including Gram-positive, Gram-negative, and hard-to-lyse species)

QCMD 16S EQA panel (reference bacterial strains for external validation)

Data Type: Nanopore long-read amplicon sequencing (full-length 16S rRNA, ~1,500 bp reads)

Pipeline Components

DNA Extraction: Performed locally with diverse in-house methods

Library Preparation: ONT 16S Barcoding Kit 24 V14 (modified protocol: 40 PCR cycles, 52 °C annealing)

Sequencing: Nanopore MinION/GridION/PromethION (FLO-MIN114 flow cells, Q score ≥10)

Quality Control: FastQC, NanoPlot, MultiQC

Taxonomic Profiling:

Commercial: 1928 Diagnostics 16S pipeline (SILVA v138.1 database)

Open-source: GMS-16S pipeline (EMU classifier, rrnDB + NCBI RefSeq databases, visualization with Krona)

How to Run

Download mock and QCMD FASTQ files from SRA (SUB14925052).

Perform read QC and filtering (1,200–1,800 bp).

Run taxonomic classification using both 1928-16S and GMS-16S pipelines.

Compare identification accuracy across pipelines.

Use questions.yaml to evaluate reproducibility and detection thresholds.

Verify outputs with answers.yaml.

References

Paper: Brunet S. et al. Nationwide multicentre study of Nanopore long-read sequencing for 16S rRNA-species identification. Eur J Clin Microbiol Infect Dis. 2025;44:1907–1916. DOI: 10.1007/s10096-025-05158-w

Open-source Pipeline: GMS-16S GitHub

Commercial Pipeline: 1928 Diagnostics

Data Source: SRA SUB14925052
