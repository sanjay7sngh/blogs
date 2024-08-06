---
title: Variant Calling from Plant Resequencing Data
date: 2024-08-06
---
 **This will be a comprehensive article on plant variant calling. It is work in PROGRESS.**

The variant calling is crucial process in genomics to identify variation at genome level that can be used for further analysis like GWAS, population genetics, genotype characterization. Genome Analysis ToolKit (GATK) is a collection of command based tools to identify variants from highthroughput sequencing data.

In this article, I have listed steps to identify genome scale variant using the GATK pipeline from Illumina sequencing data.

**Note on Genome Reference genome selection:** Write about a set of site to get plant
reference genome

**Before Starting:**  Create index sequence

    # samtools fasta index
    
    samtools faidx Brassica_juncea.ASM1870372v1.dna.toplevel.fa
    
    # bwa-mem2 for alignment index
    
    bwa-mem2 index Brassica_juncea.ASM1870372v1.dna.toplevel.fa
    
    # Picard CreateSequenceDictionary index for gatk
    
    gatk CreateSequenceDictionary  -R Brassica_juncea.ASM1870372v1.dna.toplevel.fa
    

***
Steps of Variant calling: Preprocessing Raw data; alignment; Intermediate alignment correct; Variant Calling; Variant Filter 


