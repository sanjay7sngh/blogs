---
title: Files formats in NGS data analysis
date: 2024-04-20
---

During genomic sequence data analysis, we encounter several types of file storing data of sequence, annotation, alignment and variant each serving specific purposes. In this article, in brief, I have explained the common file encountered in sequencing data analysis.


**FASTQ (.fastq):** This format contains raw sequencing reads along with quality scores. Each read is represented by four lines: a header line starting with '@', a sequence line, a separator line starting with '+', and a line containing quality scores for the corresponding sequence.

**FASTA (.fasta, .fa, .fna, .faa):** This format represents nucleotide or protein sequences. Each sequence entry starts with a header line beginning with '>', followed by the sequence data.

**SAM/BAM (.sam, .bam):** SAM (Sequence Alignment/Map) and BAM (Binary Alignment/Map) formats are used to store aligned sequence reads to a reference genome. SAM is a text-based format, while BAM is its binary equivalent. BAM files are more compact and efficient for storing large amounts of alignment data.

**VCF (.vcf):** Variant Call Format (VCF) is used to store information about genetic variants identified from NGS data. It includes details such as variant position, reference and alternate alleles, genotype information, and variant quality scores.

**BED (.bed):** Browser Extensible Data (BED) format is used to represent genomic intervals, such as regions of interest, genomic features, or variant annotations. Each entry consists of chromosome, start position, end position, and optionally additional annotation columns (first three are mandatory).

**Wiggle (WIG):** The Wiggle (WIG) file format is a text-based format commonly used in genomics and bioinformatics to represent continuous data tracks along the genome. It is often used to store data such as sequence read coverage, gene expression levels, or other genome-wide measurements.

**GFF/GTF (.gff, .gtf):** Gene Feature Format (GFF) and Gene Transfer Format (GTF) are used to describe genomic features, such as genes, transcripts, exons, and other structural elements. They include information about feature coordinates, gene IDs, and functional annotations.

**FASTA index (.fai):** This index file is associated with a FASTA file and stores metadata about the sequences, such as sequence names and lengths. It enables rapid retrieval of sequence data from large FASTA files.

**Index files:** Various alignment tools require index files for efficient data access and retrieval. Examples include BWA index files (.bwt, .pac, .ann, .amb, .sa), Bowtie index files (.ebwt), and HISAT2 index files (.ht2).

**Gene expression matrices:** These files represent gene expression data obtained from RNA-Seq experiments, typically stored as tabular formats with samples as columns and genes/transcripts as rows. Common formats include plain text (e.g., CSV, TSV) or binary formats specific to analysis tools (e.g., DESeq2, EdgeR).

**Quality control reports:** Output files from quality control tools, such as FastQC reports (.html), provide detailed information about sequence quality metrics, adapter content, and other diagnostic measures.

These are some of the key file formats encountered in NGS data analysis workflows. Understanding their structures and contents is essential for effective processing, analysis, and interpretation of NGS data.
