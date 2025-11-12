![LUMACOD](https://github.com/paolaporracciolo/LUMACOD/blob/main/MTpipeline_v5.pdf)
[View Pipeline Diagram (PDF)](MTpipeline_v5.pdf)

[![Pipeline](pipeline_thumbnail.png)](MTpipeline_v5.pdf)

# Description of the pipeline
 1. The pipeline selects high-quality mitochondrial sequencing reads.
 2. In the case of single-cell data, it selects cells with a sufficient number of read sequences to enable measurement of the heteroplasmic signal.
 3. Statistics are calculated on the filtered .bam files.
 4. On this filtered signal, it runs **mitochondrial variant calling** (calculation of *mutation frequencies*) and selects the most robust mutations (e.g., detected on both DNA strands). Then, mutation tables are produced.

The packages are installed through conda ![Conda](https://img.shields.io/badge/conda-23.5.0-green.svg) 
MT_pipeline uses: ![Python](https://img.shields.io/badge/python-3.10.14-blue.svg?logo=python&logoColor=white) ![R](https://img.shields.io/badge/R-4.5.1-blue.svg?logo=r)
It runs mitochondrial variant calling using: ![mgatk](https://img.shields.io/badge/mgatk-0.7.1-orange.svg)
