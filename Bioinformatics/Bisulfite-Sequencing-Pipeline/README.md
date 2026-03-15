# Whole Genome Bisulfite Sequencing (WGBS) Analysis Pipeline

## Overview
Whole Genome Bisulfite Sequencing (WGBS) is a powerful method used to analyze **DNA methylation patterns across the entire genome**. DNA methylation is a key epigenetic modification that regulates gene expression and plays an important role in development and disease.

This project implements a complete **bisulfite sequencing analysis pipeline using simulated data generated with Sherman**.

## Objectives
- Simulate bisulfite sequencing reads
- Perform quality control and read trimming
- Align reads to a reference genome
- Extract methylation information
- Detect differentially methylated regions (DMRs)

## Tools Used
- Sherman (BS-seq simulator)
- FastQC
- Trim Galore
- Bismark
- Bowtie2
- Samtools
- methylKit

## Workflow

### 1. Data Simulation
Bisulfite sequencing reads were simulated using **Sherman** to generate paired-end FASTQ files for control and treatment samples.

Generated datasets:
- control_1.fastq
- control_2.fastq
- treatment_1.fastq
- treatment_2.fastq

### 2. Quality Control
Quality assessment was performed using **FastQC** to evaluate read quality and sequencing artifacts.

### 3. Adapter Trimming
Low-quality bases and adapters were removed using **Trim Galore**.

### 4. Alignment
Reads were aligned to a bisulfite-converted reference genome using **Bismark with Bowtie2**.

Mapping efficiency:
≈ **93% uniquely aligned reads**

### 5. Methylation Extraction
Bismark methylation extractor identified methylated and unmethylated cytosines across the genome.

### 6. Differential Methylation Analysis
The **methylKit** package was used to identify differentially methylated regions between control and treatment samples.

### 7. Validation
Predicted DMRs were compared with simulated ground-truth regions to evaluate pipeline performance. :contentReference[oaicite:5]{index=5}

## Results
- Cytosines analyzed: ~7.2 million
- CpG methylation: ~1%
- CHG methylation: ~1%
- CHH methylation: ~1%

The pipeline successfully detected simulated differential methylation regions.

## Conclusion
This project demonstrates a complete and reproducible WGBS analysis workflow, covering all major steps from simulated read generation to differential methylation analysis.

## Author
Siddiqa Rani  
BS Bioinformatics
