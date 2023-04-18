# britroc-HGSOC-landscape
Top level repository for bioinformatic and analysis pipelines used the publication ["The copy-number landscape of recurrent ovarian high grade serous carcinoma" Smith et al. 2023]().

## Summary

The drivers of recurrence and resistance in ovarian high grade serous carcinoma (HGSC) remain unclear. We investigated the acquisition of resistance by collecting tumour biopsies from a cohort of 276 women with relapsed HGSC in the BriTROC-1 study. Panel sequencing showed close concordance between diagnosis and relapse, with only four discordant cases. There was also very strong concordance in copy number (CN) between diagnosis and relapse, with no significant difference in purity, ploidy or focal somatic CN alterations, even when stratified by platinum sensitivity or prior chemotherapy lines. CN signatures were strongly correlated with immune cell infiltration, whilst diagnosis samples from patients with primary platinum resistance had increased rates of CCNE1 and KRAS amplification and CN signature 1 exposure. Our data show that the HGSC genome is remarkably stable between diagnosis and relapse and acquired chemotherapy resistance does not select for common copy number drivers.

This repository is acts a top-level directory for the NGS data, pre-processing pipelines, analysis pipelines, and figure rendering for the publication.

## Analysis pipelines

|*Analysis*|*Details*|
|----------|---------|
|[swgs-absolutecn](https://github.com/Phil9S/swgs-absolutecn)|copy number fitting pipeline used to generated absolute copy number profiles from BAM files|
|[britroc-cn-analysis](https://github.com/BRITROC/britroc-cn-analysis)|code and scripts used to generate copy number alteration analysis markdowns and figures|
|[britroc-sig-analysis]()|code and scripts used to run differential signature abundance analysis markdowns and figures|

## Data repositories
|*Data*|*Details*|
|------|---------|
|[sWGS data]()|an EGA data repository containing hg19 aligned BAM files for the samples with available sWGS sequencing|                  
|[TAM-Seq data]()|an EGA data repository containing FASTQ files for the samples with available TAM-Seq SNV sequencing data|
|[pre-processed sWGS data](https://zenodo.org/record/7573784#.ZD6uPXbMJPY)|a zenodo repositiory containing pre-processed absolute copy number profiles from sWGS BAM files|
|[pre-processed TAM-Seq data]()|pre-processed SNV data from TAM-Seq sequencing data|

## Issues

- Data access - apply via the EGA data access commitee.
- Repository-specific issues - please open an issue on the relevant github repository.
- General questions about running the pipelines - open an issue on this repository.
- Queries directly about the paper - email the corresponding author listed on the publication.

## Authors

- [@phil9s](https://github.com/Phil9S)
- [@TBradley27](https://github.com/TBradley27)
- [@lm687](https://github.com/lm687)

## License
A vast majority of the code used in this publication is open-source and covered by GPL-3.0 license.
 
The copy number signature methodology is not and is covered by a GAP Available Source License v1.0 (see license file) as part of a pending patent application. The following text applies to the aforementioned copy number signature methodology;
 
 ```
The contents of this repository are copyright (c) 2022, University of Cambridge and Spanish National Cancer Research Centre (CNIO).

The contents of this repository are published and distributed under the GAP Available Source License v1.0 (ASL).

The contents of this repository are distributed in the hope that it will be useful for non-commercial academic research, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the ASL for more details.

The methods implemented in the code are the subject of pending patent application GB 2114203.9.

Any commercial use of this code is prohibited.
```
