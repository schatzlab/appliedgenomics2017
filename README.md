# JHU EN.600.649: Computational Genomics: Applied Comparative Genomics
[Michael Schatz](http://schatzlab.cshl.edu) (mschatz @ cs.jhu.edu) <br>
Class Hours: Tuesday + Thursday @ 1:30p - 2:45p in Shaffer 304 <br>
Office Hours: Tuesday + Thursday @ 3-4p in Malone 323 and by appointment

**The primary goal of the course is for students to be grounded in theory and leave the course empowered to conduct independent genomic analyses.** We will study the leading computational and quantitative approaches for comparing and analyzing genomes starting from raw sequencing data. The course will focus on human genomics and human medical applications, but the techniques will be broadly applicable across the tree of life. The topics will include genome assembly & comparative genomics, variant identification & analysis, gene expression & regulation, personal genome analysis, and cancer genomics. The grading will be based on assignments, a midterm exam, class presentations, and a significant class project. There are no formal course prerequisites, although the course will require familiarity with UNIX scripting and/or programming to complete the assignments and course project. 

### Prerequisites
- Online introduction to Unix/Linux. Students are strongly recommended to complete one of the following online tutorials (or both) before class begins. 
  - [Code academy's Intro to Unix](https://www.codecademy.com/en/courses/learn-the-command-line/lessons/environment/exercises/bash-profile)
  - [Command line bootcamp](http://rik.smith-unna.com/command_line_bootcamp/?id=9xnbkx6eaof)
- Access to an Apple or Linux Machine, or Install [VirtualBox](https://www.virtualbox.org/)

## Course Resources:
- [Syllabus and Policies](https://github.com/schatzlab/appliedgenomics/tree/master/policies)
- [Piazza Discussion Board](https://piazza.com/jhu/spring2017/600649/home)

## Related Courses
- [Applied Comparative Genomics by Aaron Quinlan](https://github.com/quinlan-lab/applied-computational-genomics)
- [Algorithms for DNA Sequencing by Ben Langmead](http://www.langmead-lab.org/teaching-materials/)

## Schedule
| # | Date | Lecture | Readings & Resources | Assignment |
|:--|:-----|:--------|:---------------------|:-----------|
|1. | Tu 1/31 | [Introduction](http://nbviewer.jupyter.org/github/schatzlab/appliedgenomics/blob/master/lectures/01.Introduction.pdf) | * [Biological data sciences in genome research (Schatz, 2015, Genome Research)](http://genome.cshlp.org/content/25/10/1417.full) <br> * [Big Data: Astronomical or Genomical? (Stephens et al, 2015, PLOS Biology)](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002195) | [Sign Up for Piazza](https://piazza.com/jhu/spring2017/600649/home) |
|2. | Th 2/2  | [Genomic Technologies](http://nbviewer.jupyter.org/github/schatzlab/appliedgenomics/blob/master/lectures/02.GenomicTechnologies.pdf) | * [Molecular Structure of Nucleic Acid (Watson and Crick, 1953, Nature)](http://www.nature.com/nature/dna50/watsoncrick.pdf) <br> * [Coming of age: ten years of next-generation sequencing technologies (Goodwin et al, 2016, Nature Reviews Genetics)](http://www.nature.com/nrg/journal/v17/n6/full/nrg.2016.49.html) <br> * [High‐throughput sequencing for biology and medicine (Soon et al, 2013, Molecular Systems Biology)](http://msb.embopress.org/content/9/1/640)
|3. | Tu 2/7  | [Whole Genome Assembly](http://nbviewer.jupyter.org/github/schatzlab/appliedgenomics/blob/master/lectures/03.GenomeAssembly.pdf)  | * [Velvet: Algorithms for de novo short read assembly using de Bruijn graphs (Zerbino and Birney, 2008, Genome Research)](http://genome.cshlp.org/content/18/5/821.full) <br> * [Quake: quality-aware detection and correction of sequencing errors (Kelley et al, 2010, Genome Biology)](http://genomebiology.biomedcentral.com/articles/10.1186/gb-2010-11-11-r116) <br> * Allpaths-LG: [High-quality draft assemblies of mammalian genomes from massively parallel sequence data (Gnerre et al, 2011, PNAS)](http://www.pnas.org/content/108/4/1513)  |
|4. | Th 2/9  | [Whole Genome Assembly and Alignment](https://github.com/schatzlab/appliedgenomics/blob/master/lectures/04.AssemblyAlignment.pdf) | * [Toward simplifying and accurately formulating fragment assembly. (Myers, 1995, J. Comp. Bio.)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.52.6330&rep=rep1&type=pdf) <br> * MHAP: [Assembling large genomes with single-molecule sequencing and locality-sensitive hashing](http://www.nature.com/nbt/journal/v33/n6/abs/nbt.3238.html) <br> * FALCON-unzip: [Phased diploid genome assembly with single-molecule real-time sequencing (Chin et al, 2016, Nature Methods)](http://www.nature.com/nmeth/journal/v13/n12/full/nmeth.4035.html) <br> * [Genome assembly forensics: finding the elusive mis-assembly (Phillippy et al, 2008, Genome Biology)](http://genomebiology.biomedcentral.com/articles/10.1186/gb-2008-9-3-r55) <br> * MUMmer: [Alignment of Whole Genomes (Delcher et al, 1999, NAR)](http://mummer.sourceforge.net/MUMmer.pdf) | [Assignment 1](https://github.com/schatzlab/appliedgenomics/blob/master/assignments/assignment1/README.md)
|5. | Tu 2/14 | Guest Lecture by Ben Langmead | Bowtie, BWA, SAM/BAM, IGV, etc |
|6. | Th 2/16 | Guest Lecture by Ben Langmead | Bowtie, BWA, SAM/BAM, IGV, etc |
|7. | Tu 2/21 | Variant Analysis 1 | SamTools, FreeBayes, GATK, Scalpel, CNVnator, LUMPY |
|8. | Th 2/23 | Variant Analysis 2 | 1000 Genomes, ExAC, VCFtools, ANNOVAR, CADD, FitCons, VAAST |
|9. | Tu 2/28 | Expression Analysis 1 | TopHat, Cufflinks, STAR, Trinity, Trinotate |
|10. | Th 3/2  | Expression Analysis 2 | Sailfish, Salmon, Kalisto |
|11. | Tu 3/7  | Functional Analysis 1 | Chip-seq, Methyl-seq, DNase-seq |
|12. | Th 3/9  | Functional Analysis 2 | Single Cell Analysis (Monocle, Ginkgo) |
|13. | Tu 3/14 | Genome Arithmetic | BEDTools, Plane-Sweep Alg |
|14. | Th 3/16 | Statistics for Genomics | Probability Distributions, Tests for significance, Data visualization |
| | Tu 3/21 | *Spring Break!*
| | Th 3/23 | *Spring Break!*
|15. | Tu 3/28 | Gene Regulation 1 | ChromHMM, Segway, <br> * [BUSCO: assessing genome assembly and annotation completeness with single-copy orthologs](https://academic.oup.com/bioinformatics/article/31/19/3210/211866/BUSCO-assessing-genome-assembly-and-annotation) <br> * Glimmer: [Microbial gene identification using interpolated Markov models](http://www.cs.jhu.edu/~genomics/Glimmer/glimmer-nar.pdf) <br> * [MAKER2: an annotation pipeline and genome-database management tool for second-generation genome projects](http://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-491) <br> * [What is a hidden Markov model?](http://www.nature.com/nbt/journal/v22/n10/full/nbt1004-1315.html) |
|16. | Th 3/30 | Gene Regulation 2 | ENCODE, modENCODE, GTex, Roadmap Epigenome |
|17. | Tu 4/4  | Midterm Review
|18. | Th 4/6  | Midterm Exam
|19. | Tu 4/11 | Human Evolution | Ancient Hominids, Mammalian Evolution, LUCA |
|20. | Th 4/13 | Microbiome and Metagenomics | HMP, Kraken, MEGAN, PhymmBL |
|21. | Tu 4/18 | Cancer Genomics 1 | TCGA, ICGC, Cellularity, Clonality, Tumor Evolution |
|22. | Th 4/20 | Cancer Genomics 2 | FunSeq, GECCO, HotNet |
|23. | Tu 4/25 | Genomic Futures 1 | Personalized Medicine (AlleleSeq, SnyderOme, Prenatal screeing), Genomic Privacy (Surname Inference) |
|24. | Th 4/27 | Genomic Futures 2 | Digital Immune System |
|25. | Tu 5/2  | Project Presentations 1 |
|26. | Th 5/4  | Project Presentations 2 |


