# Rare Hack

### JellyByte: David Magrefty, Ilan Mitnikov, Itamar Chinn, Liyam Chitayat

March 2024

Our tool gives scientists the ability to explore and find new research direc-
tions. We have ingested and matched protein and molecular data from various
databases, combined them with three different machine-learning models and
came up with novel algorithms for finding:  

  * Critical pathways for biomarkers of rare diseases  

  * Similarities between different rare diseases  

  * Similarities between 4200 rare diseases and 854 diseases that have been cured  

## Objectives
• Compare system effects of rare disease mutations to create bigger cohorts of patients.  

• Identify the 5,000 unknown patients who have CMT4J using biomarker analysis.  

• Identify common pathways between existing drug targets and rare disease impact to repurpose drugs  

## Methods

We have aggregated data across multiple sources for creating a graph of interactions between different genes, proteins, and molecules with the aim to emulate to
some extent biological pathways. We use the following data sources: Uniprot - Protein sequences and metadata, BioGrid - Protein-protein interactions, RHEA - Metabolic pathways, BRENDA - Metabolic pathways, ProteinAtlas - targets
of FDA approved drugs, Chebi - Metabolite metadata, PubMed - Literature, Protein Data Bank (PDB) - Protein structures, AlphaFold Database - Predicted protein structures.
The graph we build consists of:  

• Total Proteins: 14,407 + 3,357 = 17,764  

• Total Enzymes: 3,357  

• Total Molecules: 5,445  

![alt text](https://github.com/katlovescats2/Harvard-Rare-Disease-Hackathon-2024/blob/main/IDI%20Labs/Fig1_idilabs.png "Figure 1")
### Figure 1: Co-Folding of FIG4 and VAC14

On top of that graph we have implemented algorithms for finding pathways and measures of similarity between different genes. In particular we have used the following models to calculated direct interaction between proteins and
molecules to infer pathways and understand the effect of different mutations in
the same genes:  

• Using our AlphaMissense integration you will be able to predict whether
the mutation is pathogenic.  

• Using AlphaFold-Multimer we take the mutated gene and check with of
the known proteins it interacts with whether it will be able to fold with
the mutation or not. Figure. 1  

• For every protein it finds, one will be able to explore the entire pathway
that might be damaged due to the mutation.  

• Using Pesto we are able to identify the critical positions of residues for
protein-molecule interactions. If we find the mutation causing issues with
molecule interactions, one will be able to explore the entire interaction
path through our graph.  

Then for analyzing the biomarkers of a particular disease we create a measure of
connectivity between the target gene and associated molecules in the pathway. In particular, we score the significance of each biomarker through the following equation: 
P

p∈pathways
1
Length(p)
2 where pathways are different pathways
between the target gene and the molecule. We then provide a ranked list of
molecules to explore.

In addition, we do a wide scale analysis to compare between different genes
but quantifying the significance of the the connectivity of their pathways using
the following formular:
X
m∈molecuels

Deg(m)
D1(m)
2 + D2(m)
2

Where D1, D2 are the distances between a molecule and the respective genes,
and Deg(m) is the significance of a particular molecule specified by the number
of its interactions.


We ran a similar analysis to quantify the similarity of the target gene, FIG4
in our case, to other diseases for a cure is available with the hopes of finding
common pathways for available drugs which could alleviate the symptoms of
the genetic diseases.
Below Figure. 2 we show the similarity distribution of cured diseases and
the FIG4 gene. This provides an avenue for exploring symptomatic cures for
patients using market available drugs.
