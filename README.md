# Bioinformatics

This page includes bioinformatics software and pipelines optimised by the [Sydney Informatics Hub](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html), the University of Sydney for compute platforms including the University of Sydney's [High Performance Computer Artemis](https://informatics.sydney.edu.au/services/artemis/), Australia's [National Compute Infrastructure](https://nci.org.au/) (NCI), the University of Queensland's (UQ's) HPC [Flashlite](https://rcc.uq.edu.au/filething/get/14818/FlashLite_User_Guide_20200122.pdf) and AWS Cloud.

## NCI Gadi optimised pipelines

The Sydney Informatics Hub has worked alongside with the National Compute Infrastructure (NCI) team to establish fast, efficient and scalable bioinformatics workflows on NCI’s HPC, Gadi. The workflows implement best practice workflows and reputable software and are specifically designed to utilise NCI Gadi’s infrastructure optimally. The table below contains a list and descriptions of bioinformatics workflows optimised for NCI Gadi that are available on our GitHub page. 


| Repository| Description     |	Software	|
|-----------|-----------------|-----------------|
|[QC-tools](https://github.com/Sydney-Informatics-Hub/QC-tools)|Obtain fastQC reports, perform trimming, convert quality score encodings for fastq files|fastQC, multiQC, BBTools|
|[Fastq-to-BAM](https://github.com/Sydney-Informatics-Hub/Fastq-to-BAM)|Whole genome sequence alignment to a reference genome following pre-processing recommendations by the BROAD Institute|bwa-kit, fastp, BWA-MEM, SAMbamba, SAMblaster, SAMtools, GATK 4|
|[Germline-ShortV](https://github.com/Sydney-Informatics-Hub/Germline-ShortV)|Germline short variant calling (joint calling) following the Germline short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute|GATK4|
|[Bootstrapping-for-BQSR](https://github.com/Sydney-Informatics-Hub/Bootstrapping-for-BQSR)|Bootstrapping a variant resource to enable GATK base quality score recalibration (BQSR) for non-model organisms that lack a publicly available variant resource. |GATK4|
|[Somatic-ShortV](https://github.com/Sydney-Informatics-Hub/Somatic-ShortV)|Somatic short variant calling (joint calling) following the Somatic short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute for tumour-normal pairs|GATK 4|
|[Gadi-Trinity](https://github.com/Sydney-Informatics-Hub/Gadi-Trinity)|Perform de novo transcriptome assembly with Trinity|Trinity|
|[StructuralV]|TBA: Structural variant calling using MANTA, GRIDSS2 and CNVkit|Manta, GRIDSS2, CNVkit|
|[RNASeq-DE](https://github.com/Sydney-Informatics-Hub/RNASeq-DE)|Process RNA sequencing data for differential expression, including fastQC, trimming, mapping with STAR and obtaining a raw count matrix|fastQC, multiQC, bbduk, STAR, RSeQC, HTSeq|
|[BioCommons-Canu-Metrics](https://github.com/Sydney-Informatics-Hub/BioCommons-Canu-Metrics)|Collect compute resource usage metrics (CPU, memory, /scratch disk, /jobfs disk, iNode) after running Canu optimised for NCI Gadi by the Australian BioCommons||

## UQ Flashlite optimised pipelines

| Repository| Description     |	Software	|
|-----------|-----------------|-----------------|
|[Flashlite-Trinity](https://github.com/Sydney-Informatics-Hub/Flashlite-Trinity)|Perform de novo transcriptome assembly using Trinity on Flashlite using Singularity containers|Singularity v3|
|[Flashlite-Juicer](https://github.com/natbutter/juicer)|PBS version of [Juicer](https://github.com/aidenlab/juicer) that generates Hi-C maps from raw fastq files| [Juicer](https://github.com/aidenlab/juicer)|
|[Flashlite-Supernova](https://github.com/Sydney-Informatics-Hub/Flashlite-Supernova)|10X Genomic's Supernova generates phased, whole-genome de novo assemblies from a Chromium-prepared library.| Supernova |


## NCI Raijin (decommissioned) optimised pipelnes

| Repository| Description     |	Software	|
|-----------|-----------------|-----------------|
|[SIH-Raijin-Trinity](https://github.com/Sydney-Informatics-Hub/SIH-Raijin-Trinity)| Trinity assembles Illumina RNA-Seq data into transcript sequences. Trinity was developed at the Broad Institute and the Hebrew University of Jerusalem. SIH-Raijin-Trinity allows Trinity to be scalable by enabling use of multiple nodes on NCI Raijin. The entire workflow can complete ~4X faster using 10 broadwell nodes!| samtools/1.9, java/jdk1.8.0_60, bowtie2/2.3.3.1, jellyfish/2.2.6, salmon/0.11.0, perl/5.22.1, trinity/2.8.4, python3/3.6.7|

# Cite us to support us!

If you use our pipelines, please cite us:

Sydney Informatics Hub, Core Research Facilities, University of Sydney, 2021, *The Sydney Informatics Hub Bioinformatics Repository*, \<date accessed\>, <https://github.com/Sydney-Informatics-Hub/Bioinformatics>

You can also find DOIs for all our pipelines at the Sydney Informatics Hub's [WorkflowHub](https://workflowhub.eu/projects/43#workflows)

# Acknowledgements

Acknowledgements (and co-authorship, where appropriate) are an important way for us to demonstrate the value we bring to your research. Your research outcomes are vital for ongoing funding of the Sydney Informatics Hub and national compute facilities. 

Suggested acknowledgements:

__NCI Gadi__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. The authors acknowledge the use of the National Computational Infrastructure (NCI) supported by the Australian Government and the Sydney Informatics Hub HPC Allocation Scheme, supported by the Deputy Vice-Chancellor (Research), University of Sydney and the ARC LIEF, 2019: Smith, Muller, Thornber et al., Sustaining and strengthening merit-based access to National Computational Infrastructure (LE190100021).


__USyd Artemis__ 

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. This research utilised the high performance computing service, Artemis, provided by the Sydney Informatics Hub, Core Research Facility, University of Sydney.

__UQ's Flashlite__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. The authors acknowledge the use of the high performance computing services provided by the University of Queensland's Research Computing Centre (RCC).


