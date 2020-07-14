# Bioinformatics

This page includes bioinformatics software and pipelines optimised by the [Sydney Informatics Hub](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html) for compute platforms including the University of Sydney's [High Performance Computing service](https://informatics.sydney.edu.au/services/artemis/), National Compute Infrastructure and AWS.

## Acknowledgements

Acknowledgements (and co-authorship, where appropriate) are an important way for us to demonstrate the value we bring to your research. Your research outcomes are vital for ongoing funding of the Sydney Informatics Hub. If you use any SIH material towards a publication, please acknowledge the Sydney Informatics Hub.

Suggested acknowledgements:

__NCI Gadi__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney. This research utilised the National Compute Infrustructure, Gadi. 

__USyd Artemis__ 

This research was supported by the Sydney Informatics Hub and the University of Sydney’s high performance computing service, Artemis, funded by the University of Sydney.


## NCI Gadi optimised pipelines

The Sydney Informatics Hub has worked alongside with the National Compute Infrastructure (NCI) team to establish fast, efficient and scalable bioinformatics workflows on NCI’s HPC, Gadi. The workflows implement best practice workflows and reputable software and are specifically designed to utilise NCI Gadi’s infrastructure optimally. The table below contains a list and descriptions of bioinformatics workflows optimised for NCI Gadi that are available on our GitHub page. 


| Repository| Description     |	Software	|
|-----------|-----------------|-----------------|
|[QC-tools](https://github.com/Sydney-Informatics-Hub/QC-tools)|Obtain fastQC reports, perform trimming, convert quality score encodings for fastq files|fastQC, multiQC, BBTools|
|[FASTQ-BAM]|Whole genome sequence alignment to a reference genome following pre-processing recommendations by the BROAD Institute|bwa-kit, fastp, BWA-MEM, SAMbamba, SAMblaster, SAMtools, GATK 4|
|[Germline-ShortV](https://github.com/Sydney-Informatics-Hub/Germline-ShortV)|Germline short variant calling (joint calling) following the Germline short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute|GATK4|
|[Somatic-ShortV](https://github.com/Sydney-Informatics-Hub/Somatic-ShortV)|Somatic short variant calling (joint calling) following the Somatic short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute for tumour-normal pairs|GATK 4|
|[StructuralV]|TBA: Structural variant calling using MANTA, GRIDSS2 and CNVkit|Manta, GRIDSS2, CNVkit|
|[RNASeq-DE]|Process RNA sequencing data for differential expression, including fastQC, trimming, mapping with STAR and obtaining a raw count matrix|fastQC, multiQC, bbduk, STAR, RSeQC, HTSeq|

## NCI Raijin optimised pipelnes

| Github Repo| Description     |	Software	|
|-----------|-----------------|-----------------|
|[SIH-Raijin-Trinity](https://github.com/Sydney-Informatics-Hub/SIH-Raijin-Trinity)| Trinity assembles Illumina RNA-Seq data into transcript sequences. Trinity was developed at the Broad Institute and the Hebrew University of Jerusalem. SIH-Raijin-Trinity allows Trinity to be scalable by enabling use of multiple nodes on NCI Raijin. The entire workflow can complete ~4X faster using 10 broadwell nodes!| samtools/1.9, java/jdk1.8.0_60, bowtie2/2.3.3.1, jellyfish/2.2.6, salmon/0.11.0, perl/5.22.1, trinity/2.8.4, python3/3.6.7|


## Suggested workflows

Below are quick guides on how to link pipelines into workflows to process your sequencing data that is relevant to your specific research. Follow the set up guide for instructions on software installation.

### Whole genome sequencing

__Human: Calling germline variants__

__Human: Cancer research__

## Set up

### Gadi
