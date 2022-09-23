# Pbp2

This repository focus on the analysis of CRAC data measuring the RNA-binding of yeast protein, [Pbp2/Hek1](https://www.yeastgenome.org/locus/S000000437). The raw CRAC sequencing data was provided by Stefan. The raw CRAC sequencing data was processed and analysed by the [nf_CRACpipeline](https://github.com/JingQiChong/nf_CRACpipeline).

# Content

The input files for the nf_CRACpipeline to process raw CRAC data of Pbp2 and the analysis outputs from the pipeline are organised into subdirectories, and their contents are briefly described here. Each of the subdirectory has its own 'README.md' file with more detailed description (to be added). 

## input_annotation

This subdirectory stored the annotation files (transcript maps in gff/gtf format, aligner index) required for running nf_CRACpipeline on Pbp2 dataset. 

## input_barcodes

This subdirectory containes the sequencing adapters needed for running the nf_CRACpipeline on Pbp2 dataset. 

## results

The output files generated from nf_CRACpipeline are stored here.

## rmarkdown

This folder contains the rmarkdown scripts written for further analysis on Pbp2 CRAC data or producing figures. These scripts run after the nf_CRACpipeline has completed.