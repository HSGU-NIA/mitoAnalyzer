# *mitoAnalyzer*
A software package for analyses of mitochondrial DNA using sequencing data  

## Overview
mitoAnalyzer is a software package that provides a general approach for the analysis of mitochondrial DNA (mtDNA) in next-generation sequencing studies, using whole-genome sequencing data. It has two components:

* *mitoCaller* -- an algorithm designed specifically to identify mtDNA variants (i.e., homoplasmies and heteroplasmies)
mitoCaller incorporates sequencing error rates at each base in a likelihood calculation and allows allele fractions at a variant site to differ among individuals. It relies on a genotype likelihood calculation, described below: 

 ### Genotype Likelihood Calculation
 

* *mitoCalc* and *fastMitoCalc* -- programs to estimate mtDNA copy number in a cell directly from sequencing data
mitoCalc and fastMitoCalc estimate mtDNA copy number based on the observed ratios of sequence coverages between mtDNA and autosomal DNA

  The most recent update, fastMitoCalc is a program that can estimate mtDNA copy number highly accurately but is more than 100 times faster than mitoCalc. fastMitoCalc can rapidly analyze hundreds of thousands of genomes, thereby facilitating association studies of mtDNA copy number with quantitative traits or nuclear variants.

### Method for *mitoCalc* and *fastMitoCalc*

### Comparison between *mitoCalc* and *fastMitoCalc*
