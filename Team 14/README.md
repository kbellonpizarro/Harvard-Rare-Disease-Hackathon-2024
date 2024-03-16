# Neighbor FOXP1

### Author: Bhargav C N, Hitesh K
• The tool models the given variant provided as input in HGVS format by reading the fasta of the existing FOXP1 and mutating upon it.  
• The mutation sequence model is used further compare with the genes that have affiliation towards FOXP1  
• Various quanitifiable attributes are derived between these models  
• The derived attributes are presented to visualize alongside the limited dataset of severity associated with the FOXP1 variant and possible precautions to be taken. This approach
allows us to map the limited dataset (which as a whole provides for lesser correlation) to abundant data of genes which are different and provide high correlation to understand the role it plays in treatement of rare disease. 

## Internal Working
The working of the model involves three major steps:  
• Model the mutation of the gene using the input provided in HVGS format  
• Load all the models of genes that interact with FOXP1  
• Generate attributes which count for the correlation between the genes
## Usage 
Note: Requires python >=3.12  
• Install requirementspip install -r requirements.txt  
• The application is configured to use as both API and commandline tool Use command to run the local server and access APIflask run  
• Use command line by the following command flask generate --genes gatad2b,il2 --name c.532C>T p.(Gln178*) The genes are genes that foxp1 interact with and name is the HGVS format representation of FOXP1 mutation  
• Use the visual tool by running cd app/interface/foxp1  
• npm start
## Approach
Approach to find the Attributes of mutated gene variant alongside the genes that contribute
interact with the wild gene variant
The approach is considered validated due to the fact that the mutated genes have lesser
correlation with that of the wild gene. The study of the patterns arising by the comparison of
the mutated gene alongside the other major genes that the wild variant interacts with could
provide insights on how the mutation affects the functions of the other proteins.
The datasets available are lesser to build a model to understand the behaviour causes of the
fox1 syndrome. The difference in the variants and the genes it interacts with along with wild fox
p1 gene has more diverse to provide the patterns.
