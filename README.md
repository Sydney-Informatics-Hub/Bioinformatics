# Bioinformatics @ Sydney Informatics Hub

[![Sydney Informatics Hub Badge](https://img.shields.io/badge/-Sydney%20Informatics%20Hub-black?style=flat-square&logo=google-chrome&logoColor=white&link=https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html)](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html)
[![WorkflowHub Badge](https://img.shields.io/badge/-SIH_WorkflowHub-darkgreen?style=flat-square&logo=google-chrome&logoColor=yellow&link=https://workflowhub.eu/projects/43)](https://workflowhub.eu/projects/43)
[![Docker Hub Badge](https://img.shields.io/badge/-SIH_DockerHub-blue?style=flat-square&logo=docker&logoColor=white&link=https://hub.docker.com/repository/docker/sydneyinformaticshub/)](https://hub.docker.com/repository/docker/sydneyinformaticshub/)
[![YouTube Badge](https://img.shields.io/badge/-AusBioCommons_Training-darkred?style=flat-square&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UC5WlFNBSfmt3e8Js8o2fFqQ)](https://www.youtube.com/channel/UC5WlFNBSfmt3e8Js8o2fFqQ)

This page includes bioinformatics pipelines, software, and training material developed by the [Sydney Informatics Hub](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html), which is a Core Research Facility of the University of Sydney. The Sydney Informatics Hub is an official node of the [Australian BioCommons](https://www.biocommons.org.au/), and has worked in partnership with [National Computational Infrastructure](https://nci.org.au/), [Pawsey Supercomputing Research Centre](https://pawsey.org.au), and [QCIF](https://www.qcif.edu.au/) to create command-line resources that make bioinformatics more accessible for life scientists. 

Many of the resources available here are focused on making processing data at scale more accessible. To achieve this we have developed optimised pipelines for national HPC infrastructures and resources for workflow development. 

- :computer: [Reproducible pipelines for HPCs](#computer-reproducible-pipelines)
- :notebook: [Reproducible code notebooks](#notebook-reproducible-notebooks)
- :sparkles: [Supporting Nextflow](#sparkles-supporting-nextflow)
- :floppy_disk: [Software and helper scripts](#floppy_disk-software-and-helper-scripts)
- :mortar_board: [Training materials](#mortar_board-self-directed-training-materials)
- :information_desk_person: [Cite us to support us](#information_desk_person-cite-us-to-support-us)

## :computer: Reproducible pipelines 

Our pipelines have been optimised for compute platforms including the University of Sydney's HPC [Artemis](https://informatics.sydney.edu.au/services/artemis/), the [National Compute Infrastructure](https://nci.org.au/) (NCI), Pawsey Supercomputing Research Centre's HPC [Setonix](https://pawsey.org.au/systems/setonix/) and [Nimbus cloud](https://pawsey.org.au/systems/nimbus-cloud-service/), the University of Queensland's (UQ's) HPC [Flashlite](https://rcc.uq.edu.au/filething/get/14818/FlashLite_User_Guide_20200122.pdf) and AWS Cloud. You can find DOIs for all our pipelines at the Sydney Informatics Hub's [WorkflowHub](https://workflowhub.eu/projects/43#workflows). 

We also support the use of [nf-core](https://nf-co.re/) workflows. Check out the [institutional configs](https://github.com/nf-core/configs) we've build for Australian HPC and cloud infrastructures. 

|Category         |Pipeline                                                                                                |Infrastructure                                    |Description                                                                                                                                                                                                                                                                                                                    |Software                                                                                                                                                                                       |
|-----------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|Quality control  |[QC-tools](https://github.com/Sydney-Informatics-Hub/QC-tools)                                          |Optimised - NCI Gadi                              |Obtain fastQC reports, perform trimming, convert quality score encodings for fastq files                                                                                                                                                                                                                                       |fastQC, multiQC, BBTools                                                                                                                                                                       |
|Quality control  |[BamQC-nf](https://github.com/Sydney-Informatics-Hub/bamQC-nf)                                          |Nextflow - NCI Gadi, Pawsey Setonix, Pawsey Nimbus| Alignment quality control stats                                                                                                                                                                                                                                                                                               |samtools, mosdepth, qualimap, multiqc                                                                                                                                                          |
|Genomics         |[Fastq-to-BAM](https://github.com/Sydney-Informatics-Hub/Fastq-to-BAM)                                  |Optimised - NCI Gadi                              |Whole genome sequence alignment to a reference genome following pre-processing recommendations by the BROAD Institute                                                                                                                                                                                                          |bwa-kit, fastp, BWA-MEM, SAMbamba, SAMblaster, SAMtools, GATK4                                                                                                                                 |
|Genomics         |[Germline-ShortV](https://github.com/Sydney-Informatics-Hub/Germline-ShortV)                            |Optimised - NCI Gadi                              |Germline short variant calling (joint calling) following the Germline short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute                                                                                                                                                                   |GATK4                                                                                                                                                                                          |
|Genomics         |[Bootstrapping-for-BQSR](https://github.com/Sydney-Informatics-Hub/Bootstrapping-for-BQSR)              |Optimised - NCI Gadi                              |Bootstrapping a variant resource to enable GATK base quality score recalibration (BQSR) for non-model organisms that lack a publicly available variant resource.                                                                                                                                                               |GATK4                                                                                                                                                                                          |
|Genomics         |[Somatic-ShortV](https://github.com/Sydney-Informatics-Hub/Somatic-ShortV)                              |Optimised - NCI Gadi                              |Somatic short variant calling (joint calling) following the Somatic short variant discovery (SNPs + Indels) Best Practices Workflow by the BROAD Institute for tumour-normal pairs                                                                                                                                             |GATK4                                                                                                                                                                                          |
|Genomics         |Somatic-ShortV-nf                                                                                       |Nextflow - NCI Gadi, Pawsey Setonix, Pawsey Nimbus|Currently under development                                                                                                                                                                                                                                                                                                    |GATK4                                                                                                                                                                                          |
|Genomics         |[GermlineStructuralV-nf](https://github.com/Sydney-Informatics-Hub/Germline-StructuralV_nf)             |Nextflow - NCI Gadi, Pawsey Setonix, Pawsey Nimbus|Germline structural variant calling with short read bam files                                                                                                                                                                                                                                                                  |manta, smoove, tiddit, survivor, annotSV                                                                                                                                                       |
|Genomics         |[BioCommons-Canu-Metrics](https://github.com/Sydney-Informatics-Hub/BioCommons-Canu-Metrics)            |Optimised - NCI Gadi                              |Collect compute resource usage metrics (CPU, memory, /scratch disk, /jobfs disk, iNode) after running Canu optimised for NCI Gadi by the Australian BioCommons                                                                                                                                                                 |                                                                                                                                                                                               |
|Genomics         |[Flashlite-Juicer](https://github.com/natbutter/juicer)                                                 |Optimised - Flashlite [decomissioned]             |PBS version of [Juicer](https://github.com/aidenlab/juicer) that generates Hi-C maps from raw fastq files                                                                                                                                                                                                                      | [Juicer](https://github.com/aidenlab/juicer)                                                                                                                                                  |
|Genomics         |[Flashlite-Supernova](https://github.com/Sydney-Informatics-Hub/Flashlite-Supernova)                    |Optimised - Flashlite [decomissioned]             |10X Genomic's Supernova generates phased, whole-genome de novo assemblies from a Chromium-prepared library.                                                                                                                                                                                                                    | Supernova                                                                                                                                                                                     |
|RNAseq           |[RNASeq-DE](https://github.com/Sydney-Informatics-Hub/RNASeq-DE)                                        |Optimised - NCI Gadi                              |Process RNA sequencing data for differential expression, including fastQC, trimming, mapping with STAR and obtaining a raw count matrix                                                                                                                                                                                        |fastQC, multiQC, bbduk, STAR, RSeQC, HTSeq                                                                                                                                                     |
|Metagenomics     |[Shotgun-Metagenomics-Analysis](https://github.com/Sydney-Informatics-Hub/Shotgun-Metagenomics-Analysis)|Optimised - NCI Gadi                              |Analysis of metagenomic shotgun sequences including assembly, speciation, abundance, ARG discovery, functional profiling, gene prediction, insertion sequence annotation and estimation of the resitome.                                                                                                                       |abricate, bbtools, bracken, bwa, diamond, fastqc, gatk, humann2, kraken2, kronatools, megahit, metaphlan2, multiqc, nci-parallel, openmpi, prodigal, prokka, python3, sambamba, samtools, seqtk|
|Transcriptomics  |[Gadi-Trinity](https://github.com/Sydney-Informatics-Hub/Gadi-Trinity)                                  |Optimised - NCI Gadi                              |Perform de novo transcriptome assembly with Trinity                                                                                                                                                                                                                                                                            |Trinity                                                                                                                                                                                        |
|Data preparation |[IndexReferenceFasta-nf](https://github.com/Sydney-Informatics-Hub/IndexReferenceFasta-nf)              |Nextflow - NCI Gadi, Pawsey Setonix, Pawsey Nimbus| Create fasta file indexes                                                                                                                                                                                                                                                                                                     |samtools, bwa, gatk                                                                                                                                                                            |
|Biological benchmarking|[GermlineShortV_biovalidation](https://github.com/Sydney-Informatics-Hub/GermlineShortV_biovalidation)  |Optimised - Usyd Artemis                          |Biological validation of germline variant calling pipeline for model and non-model organisms.                                                                                                                                                                                                                                  |hap.py, bcftools, R                                                                                                                                                                            |                                                                                                                                                              |
## :notebook: Reproducible notebooks

|Tool             |Description                                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------------|
|[Rnaseq-rstudio](https://github.com/Sydney-Informatics-Hub/rnaseq_DE_Day2_1023.git)|A Rmarkdown notebook to convert raw gene counts to functional enrichments|

## :sparkles: Supporting Nextflow

We have created resources to support [Nextflow workflow](https://www.nextflow.io/docs/latest/index.html) development and deployment on HPC infrastructures. 

|Tool             |Description                                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------------|
|[Nextflow DSL2 template](https://github.com/Sydney-Informatics-Hub/template-nf)|A straightforward Nextflow workflow template generator.|
|[Nextflow ConfigBuilder](https://github.com/georgiesamaha/configBuilder-nf)|A simple custom config file generator. Under development.|
|[Institutional nf-core configs](https://github.com/nf-core/configs)|Public config files for running nf-core pipelines at NCI and Pawsey infrastructures. |

## :floppy_disk: Software and helper scripts 

We have created resources to support workflow development and deployment on HPCs, resource benchmarking, and flexible data visualisation. 

|Tool             |Description                                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------------|
|[HPC usage reports](https://github.com/Sydney-Informatics-Hub/HPC_usage_reports) |Pull resource usage data from HPC job logs into reports.|                                        
|[NCI Gadi benchmarking template](https://github.com/Sydney-Informatics-Hub/Gadi-benchmarking/tree/main) |Automated submission of identical benchmark tasks with increasing compute resources. |            
|[IGVreport-nf](https://github.com/Sydney-Informatics-Hub/IGVreport-nf) |Generate IGV report for a set of variants.|
|[split-GeneWiz-fastq](https://github.com/Sydney-Informatics-Hub/split-GeneWiz-fastq) |Split GeneWiz 'combined' (concatenated) fastq files into correct flowcell-lane pairs.|
|[Fix-BAM-read-groups](https://github.com/Sydney-Informatics-Hub/Fix-BAM-read-groups) |Change the read group metadata within a BAM file. Operates on the header as well as the individual SAM output lines.|

## :mortar_board: Self-directed training materials

We deliver national training events focused on the accessibility of command-line bioinformatics as a part of the Australian BioCommons training cooperative. Visit their [events page](https://www.biocommons.org.au/events) for upcoming events. You can find recordings of past events on the [Australian BioCommons YouTube channel](https://www.youtube.com/@AustralianBioCommonsChannel) and the [Sydney Informatics Hub YouTube channel](https://www.youtube.com/@sydneyinformaticshub1170). Materials for all Australian BioCommons events are published on [Zenodo](https://zenodo.org/communities/australianbiocommons-training/).

|Event            |Description                                                                                             |Prerequisites                                                 |
|-----------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
|[Unlocking nf-core workshop](https://sydney-informatics-hub.github.io/customising-nfcore-workshop/)|Foundational skills for running and customising nf-core workflows reproducibly.                         |Experince with Unix CLI, familiarity with Nextflow and nf-core|
|[Introduction to RNAseq workshop](https://sydney-informatics-hub.github.io/training.RNAseq.series-quarto/)|RNAseq data analysis for differential expression on the CLI.                                            |Experince with Unix CLI, familiarity with R/RStudio           |
|[Artemis HPC training series](https://sydney-informatics-hub.github.io/training.artemis/)|A comprehensive introduction to USyd's HPC.                                                 |Competency with Unix CLI             |
|[Introduction to NCI Gadi workshop](https://sydney-informatics-hub.github.io/training.gadi.intro/)|A quickstart guide for experienced supercomputer users.                                                  |Experience with Unix CLI, HPC infrastructures                 |
|[Pro-tips for scaling bioinformatics workflows to HPC webinar](https://youtu.be/YKJDRXCmGMo)|Essential concepts and considerations for working on HPCs.                                              |None                                                          |
|[Getting started with WGS mapping and variant calling webinar](https://www.youtube.com/watch?v=Q2EceFyizio)|Essential practical considerations for working with WGS data.                                           |None                                                          |
|[Making your workflows findable and citable webinar](https://www.youtube.com/watch?v=2kGKxaPuQN8)| An introduction to workflow registries to share your computational workflows with the research community.                                    |None                                                          |
|[Submitting your best NCMAS application](https://www.youtube.com/watch?v=HeFGjguwS0Y)|Recommendations for accessing national HPCs via NCMAS                                                   |None                                                          |
|[Where to go when your bioinformatics outgrows your compute webinar](https://www.youtube.com/watch?v=hNTbngSc-W0)|Essential concepts for understanding compute requirements of bioinformatics workflows and Australian research compute facilities|None                                                          |

## :information_desk_person: Cite us to support us!

Acknowledgements (and co-authorship, where appropriate) are an important way for us to demonstrate the value we bring to your research. Your research outcomes are vital for ongoing funding of the Sydney Informatics Hub and national compute facilities. Please cite the pipeline repository(s) that you have used. You can also find DOIs for all our pipelines at the Sydney Informatics Hub's [WorkflowHub](https://workflowhub.eu/projects/43#workflows).

Suggested acknowledgements:

__Sydney Informatics Hub__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via ARDC and Bioplatforms Australia.

__NCI Gadi__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. The authors acknowledge the use of the National Computational Infrastructure (NCI) supported by the Australian Government and the Sydney Informatics Hub HPC Allocation Scheme, supported by the Deputy Vice-Chancellor (Research), University of Sydney and the ARC LIEF, 2019: Smith, Muller, Thornber et al., Sustaining and strengthening merit-based access to National Computational Infrastructure (LE190100021).

__USyd Artemis__ 

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. This research utilised the high performance computing service, Artemis, provided by the Sydney Informatics Hub, Core Research Facility, University of Sydney.

__UQ's Flashlite__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and the Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia. The authors acknowledge the use of the high performance computing services provided by the University of Queensland's Research Computing Centre (RCC).


