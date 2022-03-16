# smr-pipeline

# Shen Lab SMR Pipeline (16 March 2022)
## Brian Lee; Xiaohui Yao, PhD; Li Shen, PhD
### Perelman School of Medicine 
### University of Pennsylvania


(MIT License applies)

Manuscript: Lee BN, Yao X, Shen L. (2022) Integrative Analysis of Summary Data from GWAS and eQTL Studies Implicates Genes Differentially Expressed in Alzheimer’s Disease. BMC Supplements. _(In review.)_

## **SMR Executable**
Download here: https://yanglab.westlake.edu.cn/software/smr/#Download (v1.03)

## **Data Resource**

### Genotyping Reference Data
Request and download PLINK files from [ADNI](adni.loni.usc.edu).

### GWAS Summary Data

Three sets of summary statistics were used:
- [IGAP Combined Dataset](www.niagads.org/datasets/ng00036).
- [Jansen et al., 2019 Summary Statistics](https://ctg.cncr.nl/software/summary_statistics)
- [Kunkle et al., 2019 Summary Statistics](https://www.niagads.org/datasets/ng00075)

### cis-eQTL Summary Data
Downloaded cis-eQTL data in [BESD format](https://yanglab.westlake.edu.cn/data/SMR/GTEx-brain.tar.gz). Other eQTL, mQTL, and caQTL datasets processed for SMR available from the data resource [webpage](https://yanglab.westlake.edu.cn/software/smr/#DataResource).

Data sourced from: [Qi, T., Wu, Y., Zeng, J. et al. Identifying gene targets for brain-related traits using transcriptomic and methylomic data from blood. Nat Commun 9, 2282 (2018). https://doi.org/10.1038/s41467-018-04558-1](https://www.nature.com/articles/s41467-018-04558-1)

## Processing Pipeline
1. Format data files as necessary -- for our pipeline, only data processing/cleaning necessary was for GWAS summary data.
2. Run SMR command with reference file dataset adni.bim / adni.bed / adni.fam, summary data set summary.ma, eQTL files qi.beqtl / qi.epi / qi.epi

```
smr --bfile adni --gwas-summary summary.ma --beqtl-summary qi --out outfile_name_here --thread-num 10
```
