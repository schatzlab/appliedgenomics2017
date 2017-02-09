## Assignment 1: Genome Assembly
Assignment Date: Thursday, Feb. 9, 2017 <br>
Due Date: Thursday, Feb. 23, 2017 @ 11:59pm <br>

### Assignment Overview

In this assignment, you are given a set of unassembled reads from a mysterious pathogen that contains a secret message encoded someplace in the genome. The secret message will be recognizable as a novel insertion of sequence not found in the reference. Your task is to assess the quality of the reads, assemble the genome, identify, and decode the secret message. If all goes well the secret message should decode into a recognizable english text, otherwise doublecheck your coordinates and try again. As a reminder, any questions about the assignment should be posted to [Piazza](https://piazza.com/jhu/spring2017/600649/home)

#### Question 1. Coverage Analysis [10 pts]

Download the reads and reference genome from: https://github.com/schatzlab/appliedgenomics/raw/master/assignments/assignment1/asm.tgz. I have provided both paired-end and mate-pairs reads (see included README for details).

- Question 1a. How long is the refernce genome? [Hint: Try samtools faidx]
- Question 1b. How many reads are provided and how long are they? Make sure to measure each file separately [Hint: Try FastQC]
- Question 1c. How much coverage do you expect to have? [Hint: see slides for formula]

#### Question 2. Kmer Analysis [10 pts]

Use Jellyfish to count the 21-mers in the reads data. Make sure to use the "-C" flag to count cannonical kmers, otherwise your analysis will not correctly account for the fact that your reads come from either strand of DNA.

- Question 2a. How many kmers occur 50 times? [Hint: try jellyfish histo]
- Question 2b. What are the top 10 most frequently occurring kmers [Hint: try jellyfish dump along with head]
- Question 2c. What is the estimated genome size based on the kmer frequencies? [Hint: upload the jellyfish histogram to GenomeScope]

#### Question 3. De novo assembly [10 pts]

Assemble the reads using ALLPATHS-LG. Allpaths will *not* run on Mac or Windows, you must use a linux environment. If you do not have access to a linux machine, download and install a virtual machine following the directions here: http://www.cs.jhu.edu/~joanne/virtualBox.html

- Question 3a. How many contigs were produced? [Hint: try 'samtools faidx', and 'wc']
- Question 3b. What is the size of your large contig? [Hint: check 'samtools faidx']
- Question 3c. What is the contig N50 size? [Hint: Write a short script, or use excel]

#### Question 4. Whole Genome Alignment [10 pts]

- Question 4a. What is the average identify of your assembly compared to the reference? [Hint: try 'dnadiff']
- Question 4b. How many insertions, deletions, and rearrangments are in the assembly? [Hint: try 'dnadiff']
- Question 4c. Make a dotplot of your assembled contigs aligned to the reference genome? [Hint: trying 'nucmer' and 'mummerplot']

#### Question 5. Decoding the insertion [10 pts]
- Question 5a. What is the position of the insertion on the reference? [Hint: try 'show-coords']
- Question 5b. How long is the novel insertion? [Hint: try 'show-coords']
- Question 5c. What is the secret message? [Hint: try 'samtools faidx' to extract the secret message, then 'dna-encode.pl -d' to decode]


### Packaging

The solutions to the above questions should be submitted as a single PDF document that includes your name, email address, and all relevant figures (as needed). Make sure to clearly label each of the subproblems and give the exact commands you used for solving the question. Submit your solutions by emailing the PDF as an attachment to "jhuappliedgenomics at gmail dot com" by 11:59pm on Feb 23. Name your PDF as "Lastname.Firstname.Asn1.pdf" (replace LastName.Firstname with your own name :-). If you submit after this time, you will start to use up your late days. Remember, you are only allowed 3 late days for the entire semester!


### Resources

- [FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/) - Raw read quality assessment
- [Jellyfish](http://www.genome.umd.edu/jellyfish.html) - Fast Kmer Counting
- [GenomeScope](http://www.genomescope.org/) - Analyze Kmer Profile to determine genome size and other properties
- [ALLPATHS-LG](http://software.broadinstitute.org/allpaths-lg/blog/?page_id=12) - Short Read Assembler. Note: Only works under linux
- [MUMmer](http://mummer.sourceforge.net/) - Whole Genome Alignment
- [SAMTOOLS](http://www.htslib.org/) - Extract part of a genome sequence using 'samtools faidx'



