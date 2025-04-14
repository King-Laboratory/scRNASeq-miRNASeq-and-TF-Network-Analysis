[comment]: <> (Hi. If you are seeing this message, please open this file with markdown preview or jupyter notebook. You can do this by right clicking on the readme file and picking 'open with'.)

# Gene Expression Analysis with RNA-Seq and Network Analysis
---------------------------------
<img src="images/module_anchor_image.png" width="400" />

## **Contents**

+ [Overview](#overview)
+ [Background](#background)
+ [Workflows](#workflows)
+ [Data](#data)
+ [Getting Started](#getting-started)
+ [Funding](#funding)
+ [License for Data](#license-for-data)

## **Overview**

The purpose of these tutorials is to help users familiarize themselves with RNA sequencing (RNA-Seq) analysis workflows using Cloud computing. Here is a link to a [YouTube video](https://youtube.com) that gives you an overview of the tutorials.

These tutorials do this by going step-by-step through specific workflows for bulk RNA-Seq, small RNA-Seq and single cell RNA-Seq (scRNA-Seq). To make these tutorials applicable to researchers who use different model organisms, we provide workflows for mouse, zebrafish and *C. elegans*. The bulk RNA-Seq and small RNA-Seq workflows cover the start to finish of basic bioinformatics analysis; starting from downloading raw sequence data, and extending to differential gene expression analysis, and producing common plots in R. For mouse, we provide transcription factor network analysis using NetAct ([Su *et al. Genome Biol.* (2022)](https://pubmed.ncbi.nlm.nih.gov/36575445/)) and scRNA-Seq workflows.

<img src="images/Cloud_Modules.png" width="800" />

## **Background**

RNA-Seq using high-throughput sequencing to characterize gene expression. Typical RNA-Seq experiments are as follows:
+ Bulk RNA-Seq - Characterization of messenger RNA (mRNA) expressed in bulk tissue(s) or cells. As more than 90% of RNA in cells are ribosomal RNA (rRNA), bulk RNA-Seq libraries deplete these rRNA using poly-A tail selection of rRNA depletion.
+ Small RNA-Seq - Characterization of mature microRNA products or other short RNAs, such as tRNA-dervied fragments, expressed in bulk tissue(s) or cells.
+ Single-Cell RNA-Seq (scRNA-Seq) - Characterization of messenger RNA (mRNA) expressed in single cells.

## **Workflows**

Our tutorials guide a user through running a particular analysis workflow for a specific dataset for either mouse, zebrafish or *C. elegans*. Each notebook demonstrates a specific workflow with instructions and code for each step in the workflow. These notebooks were designed to be run using AWS SageMaker. For more information on how to do this; navigate to the [Getting Started](#getting-started) section. Feel free to explore and run the workflows in any order you like. 

### Species-Specific Bulk RNA-Seq Workflows

#### Tutorial 1: A short introduction to downloading and mapping sequences to a transcriptome using Trimmomatic and RSEM.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_mouse.ipynb) - Mouse workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1B_alignment_full_dataset_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_full_dataset_mouse.ipynb) - Mouse workflow using the full dataset including downloading reads from SRA.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1_alignment_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_1_alignment_zebrafish.ipynb) - Zebrafish workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_1B_alignment_full_dataset_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_1_alignment_full_dataset_zebrafish.ipynb) - Zebrafish workflow using the full dataset including downloading reads from SRA.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_c_elegans.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_c_elegans.ipynb) - *C. elegans* workflow using a subset of reads.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1B_alignment_full_dataset_c_elegans.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_1_alignment_full_dataset_c_elegans.ipynb) - *C. elegans* workflow using the full dataset including downloading reads from SRA.

#### Tutorial 2: Analysis of read counts using R/DESeq2.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_mouse.ipynb) - Mouse workflow starting with read counts.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Zebrafish/Tutorial_2_DEG_zebrafish.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2_DEG_zebrafish.ipynb) - Zebrafish workflow workflow starting with read counts.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_C_elegans/Tutorial_2_DEG_c_elegans.ipynb](Bulk_RNA-Seq_C_elegans/Tutorial_2_DEG_c_elegans.ipynb) - *C. elegans* workflow workflow starting with read counts.

#### Tutorial 2B: Analysis of mouse transcription factor networks using NetAct.

[Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2B_NetAct_mouse.ipynb](Bulk_RNA-Seq_Tutorials/Bulk_RNA-Seq_Mouse/Tutorial_2B_NetAct_mouse.ipynb) - Mouse workflow starting with read counts.

### Species-Specific Small RNA-Seq Workflows

#### Tutorial 3: Analysis of small RNA-Seq reads using miRGeneDB annotation of microRNAs with R/DESeq2.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_Mouse/Tutorial_3_miRNA_mouse.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_Mouse/Tutorial_3_miRNA_mouse.ipynb) - Mouse workflow starting with read counts.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_Zebrafish/Tutorial_3_miRNA_zebrafish.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_Zebrafish/Tutorial_3_miRNA_zebrafish.ipynb) - Zebrafish workflow workflow starting with read counts.

[Small_RNA-Seq_Tutorials/Small_RNA-Seq_C_elegans/Tutorial_3_miRNA_c_elegans.ipynb](Small_RNA-Seq_Tutorials/Small_RNA-Seq_C_elegans/Tutorial_3_miRNA_c_elegans.ipynb) - *C. elegans* workflow workflow starting with read counts.

### Single Cell RNA-Seq Workflows

#### Tutorial 4: Single Cell RNA-Seq Workflows using R/seurat.

[Single_Cell_RNA-Seq_Tutorials/Single_Cell_RNA-Seq_Mouse/Tutorial_4_scRNA-Seq_mouse.ipynb](Single_Cell_RNA-Seq_Tutorials/Single_Cell_RNA-Seq_Mouse/Tutorial_4_scRNA-Seq_mouse.ipynb) - Mouse workflow starting with read counts.

## **Data**

These tutorials use example sequence data procured from the Sequence Read Archive. 

## **Getting Started**

These tutorials were designed to be used on the Amazon Web Services (AWS) Cloud computing platform and implemented using Jupyter Notebook files. Since the workflows require several freely accessible software package (e.g., Trimmomatic, STAR, etc) and many R packages, we chose to use a container where all the software is pre-installed. While having all the software pre-installed saves time, it makes the notebooks specific to a Cloud platform. We have included optional code to install of the software without using the AWS container, but it adds more than 30 minutes of runtime for some of the notebooks.

The NIGMS Sandbox team has information on AWS and running the notebooks in SageMaker using a container.

## **Funding**

Funded by NIH grant number T32 GM132006 the Maine INBRE Program (NIH/NIGMS P20 GM103423).

## **License for Data**

Text and materials are licensed under a Creative Commons CC-BY-NC-SA license. The license allows you to copy, remix and redistribute any of our publicly available materials, under the condition that you attribute the work (details in the license) and do not make profits from it. More information is available [here](https://tilburgsciencehub.com/about).

![Creative commons license](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

