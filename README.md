# NEWScoop Metagenomic Profiling Task

## Overview
This evaluation task is based on the `NEWScoop` pipeline designed for shotgun metagenomic profiling of environmental samples using raw FASTQ files. The pipeline includes quality control, host read removal, assembly, binning, and taxonomic classification.

## Dataset
- **Sample**: SRR35094901
- **Experiment**: Shotgun metagenomics of an environmental soil sample
- **Size**: ~95MB (subset provided)
- **Download Method**: `fasterq-dump SRR35094901` from NCBI SRA

## Pipeline Components
1. **Quality Control**: FastQC
2. **Host Read Removal**: Kneaddata (Bowtie2 used for filtering)
3. **Assembly**: metaSPAdes
4. **Binning**: MetaBAT2
5. **Taxonomic Profiling**: Kraken2

## How to Run
1. Download the sample FASTQ file.
2. Run through each component of the pipeline.
3. Use the provided `questions.yaml` to evaluate your results.
4. Verify with `answers.yaml`.

## References
- **Paper**: NEWScoop: A scalable workflow for shotgun metagenomic profiling of environmental samples
- **DOI**: 10.1038/s42003-025-05822-3
- **GitHub Repo**: https://github.com/newscoop/newscoop-pipeline
- **Data Source**: SRR35094901 via SRA
