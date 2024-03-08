##  Background
Charcot-Marie-Tooth, Type 4J, referred to as CMT4J, is a severe and ultra-rare type of
CMT disease. This form of hereditary neuropathy is autosomal recessive, and is estimated to
have a 1/1,000,000 chance of occurance. The disease is caused by the mutation in the FIG4
gene, leading to malfunction of malfunction in the lysosomes and peripheral nerve cells. FIG4
variants contribute to the spectrum of CMT4J, but the lack of pathogenicity data for most variant
genotypes results in diminished understanding of the relationship between genotype and
phenotype. Additionally, some individuals with different variants of FIG4 may be ineligible for
clinical trials despite having pathogenic missense variants. Hundreds of potential missense
variants could contribute to CMT4J, and statistical analyses show that CMT4J is vastly
underdiagnosed globally.
## Problem
To compensate for low sample size and lack of phenotypic data of various missense
mutations in Fig4, we aim to characterize Fig4 variants using in silico methods to offer putative
labels to variants of unknown significance (VUS) present on ClinVar using AlphaMissense.
## Data + Methods
AlphaMissense is a deep learning model adapted from AlphaFold and fine-tuned to
predict the clinical significance of missense mutations via a pathogenicity score from 0 to 1. We
apply the predictions generated from AlphaMissense onto all ClinVar and gnomAD variants of
FIG4 to generate predicted pathogenicity scores. We label 438 total variants that cause
missense mutations in the protein (single AA missense) and are able to characterize many
variants of unknown significance present in ClinVar as potentially pathogenic or benign (Fig 1).

![alt text](https://github.com/kbellonpizarro/Harvard-Rare-Disease-Hackathon-2024/blob/main/Team%207/Fig1.png "Fig 1")
### Fig 1: Mutational landscape differences between CinVar (top) and AlphaMissense (bottom) pathogenicity predictions. ClinVar predictions are majority VUS (orange), while AlphaMissense classifies most VUS into benign or pathogenic.

We also examine the entire scope of potential missense mutations across Fig4 and use AlphaMissense to evaluate pathogenicity. When doing so, we see that missense mutations to residues 480 - 550 are high pathogenicity, which corresponds to the active site and a binding
region of Vac14.

![alt text](https://github.com/kbellonpizarro/Harvard-Rare-Disease-Hackathon-2024/blob/main/Team%207/Fig2.png "Fig 2")
### Fig 2: Mutational landscape of all potential missense mutations for Fig4 and associated pathogenicity predictions

Additionally, we generate a predicted complex between Fig4 and Vac14 using MegaDock, and
enrich the structure using average pathogenicity, showing sites of high pathogenicity at the
binding region of Vac14. Additionally, the pathogenicity of I41T is very high (0.97) and present at
the Vac14 binding region (Fig 3)

![alt text](https://github.com/kbellonpizarro/Harvard-Rare-Disease-Hackathon-2024/blob/main/Team%207/Fig3.png "Fig 3")
### Fig 3: Predicted binding structure using MegaDock. Coloring by pathogenicity (red for higher values). Structure of I41T variant highlighted, and present in loop region of very high pathogenicity.
