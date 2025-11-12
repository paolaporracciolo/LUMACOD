![LUMACOD](MTpipeline_v5.svg)

$\Huge{\textsf{MT_pipeline treats scRNA-Seq and bulk RNA-Seq data.}}$
$\Huge{\textsf{It calculates low-frequency mutations in the mitochondrial genome and variations in heteroplasmy levels.}}$

Two premises 📋 for pulmonary data:
1. Random mitochondrial mutations (at low allelic frequencies) in pulmonary cells can be a proxy of damage induced by the smoke of the cigarette.
2. The smoke of the cigarette is the first cause of COPD (Chronic Obstructive Pulmonary Disease).

> [!IMPORTANT]
> On COPD data, MT_pipeline aims to identify cells and cell types that are most likely to become cancerous by using these random mutations.

# Description of the pipeline
 1. The pipeline selects high-quality mitochondrial sequencing reads.
 2. In the case of single-cell data, it selects cells with a sufficient number of read sequences to enable measurement of the heteroplasmic signal.
 3. Statistics are calculated on the filtered .bam files.
 4. On this filtered signal, it runs **mitochondrial variant calling** (calculation of *mutation frequencies*) and selects the most robust mutations (e.g., detected on both DNA strands). Then, mutation tables are produced.

## Packages info
- The packages are installed through conda ![Conda](https://img.shields.io/badge/conda-23.5.0-green.svg) 
- MT_pipeline uses: ![Python](https://img.shields.io/badge/python-3.10.14-blue.svg?logo=python&logoColor=white) ![R](https://img.shields.io/badge/R-4.5.1-blue.svg?logo=r)
- It runs mitochondrial variant calling using: ![mgatk](https://img.shields.io/badge/mgatk-0.7.1-orange.svg)
 

> [!CAUTION]
> This is the public version of the pipeline. As the pipeline is under construction, the code is in a “private” version that has not yet been published.
