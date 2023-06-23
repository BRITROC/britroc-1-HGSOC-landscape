# britroc-1-HGSOC-landscape
Top level repository for bioinformatic and analysis pipelines used the publication ["The copy-number landscape of recurrent ovarian high grade serous carcinoma"](https://www.medrxiv.org/content/10.1101/2022.10.21.22280992v1) Smith & Bradley et al. 2023.

## Summary

The drivers of recurrence and resistance in ovarian high grade serous carcinoma (HGSC) remain unclear. We investigated the acquisition of resistance by collecting tumour biopsies from a cohort of 276 women with relapsed HGSC in the BriTROC-1 study. Panel sequencing showed close concordance between diagnosis and relapse, with only four discordant cases. There was also very strong concordance in copy number (CN) between diagnosis and relapse, with no significant difference in purity, ploidy or focal somatic CN alterations, even when stratified by platinum sensitivity or prior chemotherapy lines. CN signatures were strongly correlated with immune cell infiltration, whilst diagnosis samples from patients with primary platinum resistance had increased rates of CCNE1 and KRAS amplification and CN signature 1 exposure. Our data show that the HGSC genome is remarkably stable between diagnosis and relapse and acquired chemotherapy resistance does not select for common copy number drivers.

This repository is acts a top-level directory for the NGS data, pre-processing pipelines, analysis pipelines, and figure rendering for the publication.

## Analysis pipelines

|*Analysis*|*Details*|
|----------|---------|
|[swgs-absolutecn](https://github.com/Phil9S/swgs-absolutecn/tree/publication)|copy number fitting pipeline used to generated absolute copy number profiles from BAM files|
|[britroc-1-cn-analysis](https://github.com/BRITROC/britroc-1-cn-analysis)|code and scripts used to generate copy number alteration & signature analysis markdowns and figures|
|[britroc-1-sig-analysis](https://github.com/BRITROC/britroc-1-sig-analysis)|code and scripts used to run differential signature abundance analysis markdowns and figures|
|[britroc-1-snv-analysis](https://github.com/BRITROC/BriTROC-1_short_variant_discovery)|code and scripts used to generate the SNV calls and perform analysis|

## Database repositories

|*Database Repository*|*Details*|
|----------|---------|
|[BriTROC-1 DB](https://github.com/BRITROC/BriTROC-1_DB)|A repository for building the BriTROC-1 database of BriTROC-1 metadata elements from source code and corresponding data|

## Data repositories
|*Data*|*Details*|
|------|---------|
|[sWGS data]|an EGA data repository containing hg19 aligned BAM files for the samples with available sWGS sequencing|                  
|[TAM-Seq data]|an EGA data repository containing FASTQ files for the samples with available TAM-Seq SNV sequencing data|
|[pre-processed sWGS data](https://zenodo.org/record/7573784#.ZD6uPXbMJPY)|a zenodo repositiory containing pre-processed absolute copy number profiles from sWGS BAM files|
|[pre-processed TAM-Seq data]|pre-processed SNV data from TAM-Seq sequencing data|

## Installation and dependecies
### Software dependencies
Software versions and dependencies are installed independently for each analysis or pipeline using conda.
These pipelines have been tested on cent0S linux 7.8 & RHEL 7 linux OS

Each repositiory provides its own installation instructions on installation of required software environments, additional software package and data requirements and implementations. See the README.md documents for each specific analysis for more details.

### Runtime
Required runtime for replicating the results of this publication are approximately 4 hours on a High performance computing server (6-8 hours on a high-spec laptop).
Full runtime from raw data will vary considerably on implementation, available hardware, and data processing during non-scripted analyical steps.

### Demo
No demo sofware or data is provided for the pipelines associated with this publication. All data is freely available (as pre-processed outputs) or upon request via EGA. 

## Issues

- Data access
  - Raw sequencing files - apply via the EGA data access commitee.
  - Pre-processed data - donwload directly from open-access repositories.
- Repository-specific issues - please open an issue on the relevant github repository.
- General questions about running the pipelines - open an issue on this repository.
- Queries directly about the paper - email the corresponding author listed on the publication.

## Authors

- [@phil9s](https://github.com/Phil9S)
- [@TBradley27](https://github.com/TBradley27)
- [@lm687](https://github.com/lm687)

## Citation
This repository is citable using the DOI [10.5281/zenodo.7942206](https://doi.org/10.5281/zenodo.7942206).

## License
A vast majority of the code used in this publication is open-source and covered by GPL-3.0 license.
 
The [copy number signature methodology](https://github.com/markowetzlab/CINSignatureQuantification) is covered by a GAP Available Source License v1.0 ([see here](https://github.com/markowetzlab/CINSignatureQuantification/blob/main/LICENSE)) as part of a pending patent application. This license limitation applys to the copy number signature methodology used in the [copy number analysis pipeline](https://github.com/BRITROC/britroc-cn-analysis).
