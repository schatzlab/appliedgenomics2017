# Project Ideas

Here are a few selected projects organized by theme, although you are also free to present your own project ideas. A good project is one that (1) has a well defined goal; (2) has a well defined method proposed for solving it; and (3) has appropriate data available. If any of these three characteristics are not available, your project will not be successful in the timing remaining for class. A successful model for the class project is to apply a technique developed in a different context to the biological problem of your choice. Another successful model is to identify an important paper of interest and then try to improve apon their method in some way (faster, less memory, more sensitive, more precise, etc).


## Basecalling and signal processing

1. Develop an improved base calling for Oxford Nanopore or PacBio sequencing using recurrent neural networks or other ML approach

2. Align the raw signal from Oxford Nanopore or PacBio reads to a reference genome to improve variant detection, detect methlyation, and/or polishing


## Genome assembly and variant calling

1. Extend GenomeScope to infer the genome characteristics of genomes with higher ploidy

2. Extend FALCON and develop a de novo genome assembler for polyploid genomes

3. Develop a scaffolder that can use long range information from 10X or HiC 

4. Develop methods for phasing structural variations

5. Extend Alleleseq pipeline to embed phased structural variations into a reference genome

6. Benchmark several SV callers, and create a classifier for identifying high confidence from low confidence SV calls

7. Given a catalog of known SVs, test for presence/absence of those variants in a novel sample. Does this improve accuracy over calling the variant using a single reference?

8. Jointly analyze (de novo assemble or index the raw reads) the genomes of multiple varieties of rice at once to identify sequences not present in the reference genome.

9. Studying the performanc of using the MinHash algorithm to bin long reads for copy number analysis


## Functional Genomics

1. Develop a EM based method for RNAseq analysis, and output the fractional assignments of reads to transcripts in the BAM file

2. Benchmark different RNA-seq aligners when using a phased diploid genome compared to a standard reference genome

3. Develop a RNA-seq aligner that incorporates variants known from the population (graph genome)

4. Develop methods to identify genome variants from RNAseq data, apply to individuals with many tissues profiled to identify somatic mutations

5. Run ChommHMM on a phased diploid genome (NA12878) and evaluate how that compares to annotating the reference genome

6. Develop ChromHMM postprocessing algorithm to label the states with their biological functions

7. Reproduce the results from the Monocle paper, and experiment with how well it performs using lower amounts of coverage.


## Human Evolution and Disease Genomics

1. Disease Genomics: Benchmark different non-coding mutation analysis schemes on a collection of diseased genomes

2. Cancer Genomics: Develop methods for identifying somatic mutations using high error long reads (PacBio or Oxford Nanopore)

3. Metagenomics: Evaluate sailfish/kallisto-style approaches for inferring the abundance of different species present in a population

4. Develop a new metagenomics classifier using deep learning or other advanced ML techniques.

5. Accelerate an important genomics pipeline using GPUs or cloud computing and use that to study a larger dataset


## Biologically inspired computing

1. Evaluate the methods for storing binary data as DNA sequences, and improve on them using long read sequencing 

2. Evaluate the amount of "junk data" in several widely used software packages


## Or your own idea!
