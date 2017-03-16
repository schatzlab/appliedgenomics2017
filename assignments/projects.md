# Project Ideas

Here are a few selected projects organized by theme, although you are also free to present your own project ideas. A good project is one that (1) has a well defined goal; (2) has a well defined method proposed for solving it; and (3) has appropriate data available. If any of these three characteristics are not available, your project will not be successful in the timing remaining for class. A successful model for the class project is to apply a technique developed in a different context to the biological problem of your choice. Another successful model is to identify an important paper of interest and then try to improve apon their method in some way (faster, less memory, more sensitive, more precise, etc).

## Basecalling and signal processing

1. Develop an improved base calling for Oxford Nanopore or PacBio sequencing using recurrent neural networks or other ML approach

2. Align the raw signal from Oxford Nanopore or PacBio reads to a reference genome to improve variant detection and/or polishing



## Genome Assembly and variant calling

1. Extend GenomeScope to infer the genome characteristics of genomes with higher ploidy

2. Extend FALCON and develop a de novo genome assembler for polyploid genomes

3. Develop a scaffolder that can use long range information from 10X or HiC 

4. Develop methods for phasing structural variations

5. Extend Alleleseq pipeline to embed phased structural variations into a reference genome

6. Create a classifier for identifying high confidence from low confidence structural variation calls using different technologies and pipelines

7. Given a catalog of known SVs, test for presence/absence of those variants in a novel sample. Does this improve accuracy over calling the variant using a single reference?

8. MinHash Something


## Functional Genomics

1. Evaluate different strategies for aligning RNA-seq and other functional data to a phased diploid genome

2. Evaluate the impact of aligning RNA-seq and other functional data to a graph genome

3. Develop methods to identify genome variants from RNAseq data, apply to individuals with many tissues profiled to identify somatic mutations

4. Develop ChromHMM postprocessing algorithm to label the states with their biological functions



## Human Evolution and Disease Genomics

1. Evaluate non-coding methods

2. Create an adaptive segmentation method for identifying CNVs from single cell copy number data

3. Evaluate sailfish/kallisto-style approaches for metagenomics

4. Other cancer studies

5. Analysis of other human diseases





## Biologically inspired computing

1. Evaluate the methods for storing binary data as DNA sequences, and improve on them using long read sequencing 

2. Evaluate the amount of "junk bits" in variety of widely used software packages


## Computational power

1. Accelerate an important genomics pipeline using GPUs or cloud computing and use that to study a larger dataset

2. Visualization something

## Or your own idea!
