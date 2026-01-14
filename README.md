# Bioinformatics @ Sydney Informatics Hub

[![Sydney Informatics Hub Badge](https://img.shields.io/badge/-Sydney%20Informatics%20Hub-black?style=flat-square&logo=google-chrome&logoColor=white&link=https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html)](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html)
[![WorkflowHub Badge](https://img.shields.io/badge/-SIH_WorkflowHub-darkgreen?style=flat-square&logo=google-chrome&logoColor=yellow&link=https://workflowhub.eu/projects/43)](https://workflowhub.eu/projects/43)
[![Docker Hub Badge](https://img.shields.io/badge/-SIH_DockerHub-blue?style=flat-square&logo=docker&logoColor=white&link=https://hub.docker.com/repository/docker/sydneyinformaticshub/)](https://hub.docker.com/repository/docker/sydneyinformaticshub/)
[![YouTube Badge](https://img.shields.io/badge/-AusBioCommons_Training-darkred?style=flat-square&logo=youtube&logoColor=white&link=https://www.youtube.com/channel/UC5WlFNBSfmt3e8Js8o2fFqQ)](https://www.youtube.com/channel/UC5WlFNBSfmt3e8Js8o2fFqQ)

This page includes bioinformatics pipelines, software, and training material developed by the [Sydney Informatics Hub](https://www.sydney.edu.au/research/facilities/sydney-informatics-hub.html), which is a Core Research Facility of the University of Sydney. The Sydney Informatics Hub is an official node of [Australian BioCommons](https://www.biocommons.org.au/). 

Many of the resources available here are focused on making processing data at scale more accessible. To achieve this we have developed optimised pipelines for national HPC infrastructures and resources for workflow development. 

- :pencil2: [Bioinformatics training](#pencil2-bioinformatics-training)
- :computer: [Data processing pipelines](#computer-bioinformatics-pipelines)
- :notebook: [Analytical notebooks](#notebook-analytical-notebooks)
- :sparkles: [Supporting Nextflow](#sparkles-supporting-nextflow)
- :floppy_disk: [Software and helper scripts](#floppy_disk-software-and-helper-scripts)
- :neckbeard: [Bio-toolkit resources](https://github.com/Sydney-Informatics-Hub/Bio-toolkit)
- :information_desk_person: [Cite us to support us](#information_desk_person-cite-us-to-support-us)

## :pencil2: Bioinformatics training

We deliver free training to a national audience. See our [training webpage](https://sydney-informatics-hub.github.io/bioinformatics-training/) for our events and materials.

## :computer: Bioinformatics pipelines 

Our pipelines have been optimised for compute platforms including the [National Compute Infrastructure](https://nci.org.au/) (NCI) and Pawsey Supercomputing Research Centre's HPC [Setonix](https://pawsey.org.au/systems/setonix/). 

You can find all our pipelines at the Sydney Informatics Hub's [WorkflowHub](https://workflowhub.eu/projects/43#workflows) page. 

We also support the use of [nf-core](https://nf-co.re/) workflows. Check out the [institutional configs](https://github.com/nf-core/configs) we've build for Australian HPC and cloud infrastructures. 

* [NCI Gadi HPC](https://nf-co.re/configs/nci_gadi/) 
* [Pawsey Setonix HPC](https://nf-co.re/configs/pawsey_setonix/)

## :notebook: Analytical notebooks

|Notebook             |Description                                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------------|
|[Rnaseq: differential expression](https://github.com/Sydney-Informatics-Hub/rna-differential-expression-Rnotebook)|A Rmarkdown notebook to convert raw gene counts to functional enrichments|
|[single cell RNAseq: differential expression etc](https://github.com/Sydney-Informatics-Hub/scrna-analysis)|A Rmarkdown notebook to convert raw counts to functional enrichments |
|[Proteomics: differential abundance]()|Currently under development |

## :sparkles: Supporting Nextflow

We have created resources to support [Nextflow workflow](https://www.nextflow.io/docs/latest/index.html) development and deployment on HPC infrastructures. 

|Tool             |Description                                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------------|
|[Nextflow DSL2 template](https://github.com/Sydney-Informatics-Hub/template-nf)|A straightforward Nextflow workflow template generator.|
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

## :information_desk_person: Cite us to support us!

Acknowledgements (and co-authorship, where appropriate) are an important way for us to demonstrate the value we bring to your research. Your research outcomes are vital for ongoing funding of the Sydney Informatics Hub and national compute facilities. Please cite the pipeline repository(s) that you have used. You can also find DOIs for all our pipelines at the Sydney Informatics Hub's [WorkflowHub](https://workflowhub.eu/projects/43#workflows).

Suggested acknowledgements:

__Sydney Informatics Hub__

The authors acknowledge the technical assistance provided by the Sydney Informatics Hub, a Core Research Facility of the University of Sydney and Australian BioCommons which is enabled by NCRIS via Bioplatforms Australia.

__NCI__

This research was conducted on resources of the National Computational Infrastructure (NCI), an NCRIS-enabled capability supported by the Australian Government. Access to these resources was provided by the Sydney Informatics Hub, a Core Research Facility of The University of Sydney as supported by the Deputy Vice-Chancellor (Research).

__Pawsey__

This research was conducted on resources of the Pawsey Supercomputing Research Centre, an NCRIS-enabled capability supported by the Australian Government. Access to these resources was provided by the Sydney Informatics Hub, a Core Research Facility of The University of Sydney as supported by the Deputy Vice-Chancellor (Research).
