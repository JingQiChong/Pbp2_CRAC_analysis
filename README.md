# Pbp2

This repository focus on the analysis of CRAC data measuring the RNA-binding of yeast protein, [Pbp2/Hek1](https://www.yeastgenome.org/locus/S000000437). The raw CRAC sequencing data was provided by Stefan Bresson. The raw CRAC sequencing data was processed and analysed by the [nf_CRACpipeline](https://github.com/JingQiChong/nf_CRACpipeline).

To run nf_CRACpipeline on Pbp2 CRAC data as in this repository, use this code and don't forget to install nf_CRACpipeline before running: 

```
nextflow run ~/nf_CRACpipeline/main.nf \
--reads raw.fastq \
--adapterfile input_barcodes/3primeadapter.fasta \ 
--barcode input_barcodes/barcodes.txt \ 
--mismatches 0 \ 
--novoindex input_annotation/Saccharomyces_cerevisiae.EF4.74.dna.toplevel.shortChrNames.novoindex \
--transcriptgff input_annotation/abundant_verified_full-ORF_ypd_plus_other_fixed_UTR_length_transcripts.gff \
--gtf input_annotation/Saccharomyces_cerevisiae.EF4.74_SGDv64_CUTandSUT_withUTRs_noEstimates_antisense_intergenic_4xlncRNAs_final.pyCheckGTFfile.output.quotefix.gtf \
--chromosome input_annotation/Saccharomyces_cerevisiae.EF4.74.dna.toplevel.shortChrNames.lengths \
--genelist input_annotation/Pbp2_TargetGeneNamesOnly.txt \
--genometab input_annotation/Saccharomyces_cerevisiae.EF4.74.dna.toplevel.shortChrNames.fa.tab

```

# Content

The input files for the nf_CRACpipeline to process raw CRAC data of Pbp2 and the analysis outputs from the pipeline are organised into subdirectories, and their contents are briefly described here. Each of the subdirectory has its own `README.md` file with more detailed description. 

## input_annotation

This subdirectory stored the annotation files (transcript maps in gff/gtf format, aligner index) required for running nf_CRACpipeline on Pbp2 dataset. 

## input_barcodes

This subdirectory containes the sequencing adapters needed for running the nf_CRACpipeline on Pbp2 dataset. 

## results

The output files generated from nf_CRACpipeline are stored here.

## rmarkdown

This folder contains the rmarkdown scripts written for further analysis on Pbp2 CRAC data or producing figures. These scripts run after the nf_CRACpipeline has completed.