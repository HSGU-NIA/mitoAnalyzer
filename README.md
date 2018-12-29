# *mitoAnalyzer*
A software package for analyses of mitochondrial DNA using sequencing data  

## Overview
mitoAnalyzer is a software package that provides a general approach for the analysis of mitochondrial DNA (mtDNA) in next-generation sequencing studies, using whole-genome sequencing data. It has two components:

* ***mitoCaller*** -- an algorithm designed specifically to identify mtDNA variants (i.e., homoplasmies and heteroplasmies)
*mitoCaller* incorporates sequencing error rates at each base in a likelihood calculation and allows allele fractions at a variant site to differ among individuals. It relies on a genotype likelihood calculation, described below: 

### Genotype Likelihood Calculation
![Genotype Likelihood Calculation](/images/mitoCaller_web.jpg)

* ***mitoCalc*** and ***fastMitoCalc*** -- programs to estimate mtDNA copy number in a cell directly from sequencing data
*mitoCalc* and *fastMitoCalc* estimate mtDNA copy number based on the observed ratios of sequence coverages between mtDNA and autosomal DNA

  *fastMitoCalc* is an upgraded version of *mitoCalc* that can estimate mtDNA copy number as accurately as *mitoCalc* but is over 100 times faster. *fastMitoCalc* can rapidly analyze hundreds of thousands of genomes, thereby facilitating association studies of mtDNA copy number with quantitative traits or nuclear variants.

### Method for *mitoCalc* and *fastMitoCalc*
![mitoCalc and fastMitoCalc method](/images/mitoCalc_method.jpg)

### Comparison between *mitoCalc* and *fastMitoCalc*
Program | Nuclear Genome Used as Reference | Total Length of Nuclear Genome Considered | Computing Time: 1 Sample at 4x Coverage, 1 CPU | Computing Time: 50,000 Samples at 30x Coverage, 500 CPUs
--- | --- | --- | --- | ---
*mitoCalc* | Whole genome | 3.2 billion bases | 3 hours | 3 months
*fastMitoCalc* | 3,000 1kb fragments (default setting) | 3 million bases | 59 seconds | 12.5 hours

*fastMitoCalc* is over 180x faster than mitoCalc using default settings!

## Current Directions
The software package was originally developed to analyze whole-genome sequencing data. We are actively investigating its applicability to exome-sequencing data. 

## Citation
Ding J*, Sidore C, Butler TJ, Wing MK, Qian Y, Meirelles O, Busonero F, Tsoi LC, Maschio A, Angius A, Kang HM, Nagaraja R, Cucca F, Abecasis GR, Schlessinger D* (2015). Assessing mitochondrial DNA variation and copy number in lymphocytes of ~2,000 Sardinians using tailored sequencing analysis tools. PLoS Genetics 11(7): e1005306.
\*corresponding author  
[Link to article](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1005306)

Qian Y, Butler TJ, Opsahl-Ong K, Giroux N, Sidore C, Nagaraja R, Cucca F, Ferrucci L, Abecasis GR, Schlessinger D, Ding J*(2017). fastMitoCalc: an ultra-fast program to estimate mitochondrial DNA copy number from whole-genome sequences. Bioinformatics.  
\*corresponding author  
[Link to article](https://www.ncbi.nlm.nih.gov/pubmed/28453676)

__Last update: April 14, 2017__
