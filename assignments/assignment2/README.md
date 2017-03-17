## Assignment 2: Variant Analysis
Assignment Date: Tuesday, March 7, 2017 <br>
Due Date: Thursday, March 16, 2017 @ 11:59pm <br>

### Assignment Overview

In this assignment, you are will identify variants in a human genome and then analyze the properties for them. **Make sure to show your work in your writeup!** As before, any questions about the assignment should be posted to [Piazza](https://piazza.com/jhu/spring2017/600649/home)

Some of the tools you will need to use only run in a linux environment. If you do not have access to a linux machine, download and install a virtual machine following the directions here: https://github.com/schatzlab/appliedgenomics/blob/master/assignments/virtualbox.md


#### Question 1. Gene Annotation Preliminaries [10 pts]

Download the annotation of build 38 of the human genome from here: <br>
[ftp://ftp.ensembl.org/pub/release-87/gtf/homo_sapiens/Homo_sapiens.GRCh38.87.gtf.gz](ftp://ftp.ensembl.org/pub/release-87/gtf/homo_sapiens/Homo_sapiens.GRCh38.87.gtf.gz)

- Question 1a. How many many GTF data lines are in this file? [Hint: The first few lines in the file beginning with "#" are so-called "header" lines describing thing like the creation date, the genome version (more on that later in the course), etc. Header lines should not be counted as data lines.]

- Question 1b. How many annotated protein coding genes are on each chromosome of the human genome? [Hint: Protein coding genes will contain the following text: gene_biotype "protein_coding"]

- Question 1c. What is the maximum, minimum, mean, and standard deviation of the span of protein coding genes? [Hint: use the same genes as those identified in 1b]

- Question 1d. What is the maximum, minimum, mean, and standard deviation in the number of exons for protein coding genes? [Hint: you should separately consider each isoform for each protein coding gene]


#### Question 2. Genome Sequence Analysis [10 pts]

Download chromosome 22 from build 38 of the human genome from here: <br>
[http://hgdownload.cse.ucsc.edu/goldenPath/hg38/chromosomes/chr22.fa.gz](http://hgdownload.cse.ucsc.edu/goldenPath/hg38/chromosomes/chr22.fa.gz)

- Question 2a. What is the length of chromosome 22? [Hint: You should include Ns in the length]

- Question 2b. How many Ns are in chromosome 22? What is the GC content? [Hint: You should exclude Ns when computing GC content)

- Question 2c. Restriction enzymes cleave DNA molecules at or near a specific sequence of bases. For example, the HindIII enzyme cuts at the "/" in either this motif: 5'-A/AGCTT-3' or its reverse complement, 3'-TTCGA/A-5'. How many perfectly matching HindIII restriction enzyme cut sites are there on chr22? 

- Question 2d. How many HindIII cut sites are there on chr22, assuming that a mutant form of HindIII will tolerate a mismatch in the second position? Think about ways in which you could best test for all the possible DNA combinations. [Hint: There are many valid approaches]


#### Question 3. Small Variant Analysis [10 pts]

Download the read set from here:<br> 
[http://schatzlab.cshl.edu/data/teaching/sample.tgz](http://schatzlab.cshl.edu/data/teaching/sample.tgz)

For this question, you may find this tutorial helpful: <br>
[http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html](http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html)

- Question 3a. How many single nucleotide and indel variants does the sample have? [Hint: Align reads using `bwa mem`, identify variants using `freebayes`, filter using `vcffilter -f "QUAL > 20"`, and summarize using `vcfstats`; Make sure to set the read group when running bwa mem: `bwa mem -R "@RG\tID:id\tSM:sample\tLB:lib" chr22.fa pair.1.fq pair.2.fq`]

- Question 3b. How many of the variants fall into genes? How many fall into exons? [Hint: `bedtools`]
 
- Question 3c. What is the [transition/transversion ratio](https://www.mun.ca/biology/scarr/Transitions_vs_Transversions.html) of the variants in protein coding genes? What is the ratio of variants in the exons? [Hint: try `bedtools` and `vcfstats`]

- Question 3d. Does the sample have any 'nonsense' or 'missense' mutations? [Hint: try the [Variant Effect Predictor](http://useast.ensembl.org/Tools/VEP) using the `Gencode basic transcripts`]


#### Question 4. Structural Variation Analysis [10 pts]

For this question, you should use the same reads and `bwa mem` alignments as question 3.

- Question 4a. Plot the copy number status of the sample across the chromosome divided into 10kbp bins [Hint: your plot should show how many reads align to bases 1-10k, 10k-20k, 20k-30, etc]

- Question 4b. Which gene(s) have copy number amplifications? [Hint: report all genes that have even 1bp amplified compared to the 10kbp segmentation from question 4a]

- Question 4c. How many structural variations are in the sample can be found using `lumpy`? [Hint: follow the description on the lumpy website]

- Question 4d. How many genes have structural variation breakpoints in them? [Hint: `bedtools`]


#### Question 5. De novo mutation analysis [10 pts]

For this question, we will be focusing on the de novo variants identified in this paper:<br>
[http://www.nature.com/articles/npjgenmed201627](http://www.nature.com/articles/npjgenmed201627)

Download the de novo variant positions from here (Supplementary Table S4):<br>
[http://www.nature.com/article-assets/npg/npjgenmed/2016/npjgenmed201627/extref/npjgenmed201627-s3.xlsx](http://www.nature.com/article-assets/npg/npjgenmed/2016/npjgenmed201627/extref/npjgenmed201627-s3.xlsx)

Download the annotation of regulatory variants from here:<br>
[ftp://ftp.ensembl.org/pub/release-87/regulation/homo_sapiens/homo_sapiens.GRCh38.Regulatory_Build.regulatory_features.20161111.gff.gz](ftp://ftp.ensembl.org/pub/release-87/regulation/homo_sapiens/homo_sapiens.GRCh38.Regulatory_Build.regulatory_features.20161111.gff.gz)

- Question 5a. How many variants are in protein coding genes? [Hint: convert xlsx to BED, then `bedtools`]

- Question 5b. How many variants are in *any* annotated regulatory regions? [Hint: `bedtools`]

- Question 5c. What type of annotated regulatory region has the most variants? [Hint: `bedtools`]

- Question 5d. Is this a statistically significant number of variants (P-value < 0.05)? [Hint: try simulating the same number of variants as the original file 100 times, and see how many fall into this regulatory type. If at least this many variants fall into this feature type more than 5% of the trials, this is not statistically significant]


### Packaging

The solutions to the above questions should be submitted as a single PDF document that includes your name, email address, and all relevant figures (as needed). Make sure to clearly label each of the subproblems and give the exact commands you used for solving the question. Submit your solutions by emailing the PDF as an attachment to "jhuappliedgenomics at gmail dot com" by 11:59pm on March 14. Name your PDF as "Lastname.Firstname.Asn2.pdf" (replace LastName.Firstname with your own name :-). If you submit after this time, you will start to use up your late days. Remember, you are only allowed 3 late days for the entire semester!


### Resources

#### [FreeBayes](https://github.com/ekg/freebayes) - Small Variant Identification

Make sure to install `cmake` before attempting to build.

```
$ sudo apt-get install cmake
$ git clone --recursive git://github.com/ekg/freebayes.git
$ cd freebayes
$ make
$ bin/freebayes -f chr22.fa sample.bam > sample.vcf
```

#### [VCFLib](https://github.com/vcflib/vcflib) - VCF Filtering and Querying

Downloaded with FreeBayes, provides `vcffilter` and `vcfstats`. Note that many of the tools use a shared libary in the htslib directory, so you will need to set the `LD_LIBRARY_PATH` to be able to run the command.

```
## Downloaded with FreeBayes
$ cd freebayes/vcflib
$ make
$ LD_LIBRARY_PATH=freebayes/vcflib/tabixpp/htslib freebayes/vcflib/bin/vcffilter
```


#### [BEDTools](http://bedtools.readthedocs.io/en/latest/) - Genome Arithmetic

After downloading make sure to make the script executable so you can run it on the command line:

```
$ wget https://github.com/arq5x/bedtools2/releases/download/v2.26.0/bedtools-2.26.0.tar.gz
$ tar xzvf bedtools-2.26.0.tar.gz
$ cd bedtools2
$ make
$ bin/bedtools
```

#### [Variant Effect Predictor](http://useast.ensembl.org/Tools/VEP) - Variant Interpretation

Nothing to install, just upload the VCF

#### [SnpEff](http://snpeff.sourceforge.net/SnpEff.html) - Variant Interpretation

Note that the first time you run this, it will need to download a database of variant information that can take a few minutes

```
$ wget http://sourceforge.net/projects/snpeff/files/snpEff_latest_core.zip
$ unzip snpEff_latest_core.zip
$ snpEff/scripts/SnpEff eff -v -useLocalTemplate -stats sample.vcf.html GRCh38.86 sample.vcf 
```

#### [BWA](http://bio-bwa.sourceforge.net/) - Short read aligner

Lets just install it via `apt` 

```
$ sudo apt install bwa
```


#### [Lumpy](https://github.com/arq5x/lumpy-sv) - Structural Variation Detection

Lumpy requires that samtools and sambamba are installed. You should have samtools installed from assignment 1. To install sambamba, you will first need to install the `lcd` package, which is a compiler for the D programming language.

See the documentation [here](https://github.com/arq5x/lumpy-sv) to see how to make the splitters.bam and discordants.bam files from your sample.bam file.

```
# Install ldc and sambamba
$ sudo apt-get install ldc
$ git clone --recursive https://github.com/lomereiter/sambamba.git
$ cd sambamba
$ git clone https://github.com/dlang/undeaD
$ make sambamba-ldmd2-64
$ build/sambamba
$ cd ..

# Install lumpy - note you have to manually configure htslib first
$ sudo apt install autoconf libcurl4-openssl-dev libssl-dev
$ git clone --recursive https://github.com/arq5x/lumpy-sv.git
$ cd lumpy-sv
$ cd lib/htslib/
$ autoreconf
$ cd ../../
$ make

# Run lumpy, note you will need to edit your lumpyexpress config file with the paths to samtools and sambamba
$ lumpyexpress \
    -B my.bam \
    -S my.splitters.bam \
    -D my.discordants.bam \
    -o output.vcf
```
