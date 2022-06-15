# 2022-topic-02-team-02
The aim of this analysis is to find differences in gene expression and pathway activity in 
1. 33 different cancer types (pan-cancer analysis)
2. normal and tumor tissue of KIRC patients

## Data Cleaning
### Pan-cancer analysis
1. Filter for biotypes with BiomaRt $\\rightarrow$ select only protein coding genes
2. Filter for low variance genes $\\rightarrow$ keep only upper p50 quantile
3. Results in 9741 (genes) x 9783 (patients) matrix
### KIRC data
1. Filter for biotypes with BiomaRt $\\rightarrow$ select only protein coding genes
2. Throwing out constantly expressed genes
3. Results in 19186 x 72 matrix
 
## Descriptive Analysis
### Pan-cancer analysis
Visualization of data distribution and cleaning steps
1. Box plot of mean expression of all cancer types
2. Mean/variance plot and violin plot showing the cleaning steps
### KIRC data
Volcano plot (FC against pv) to visualize (significant) differences in gene expression of tumor and normal tissue

## Findig Data Structures 
### Pan-cancer analysis
Finding clusters of patients, visualize similarities/differences between tumor types
1. PCA 
2. UMAP on PCs
### KIRC data
PCA shows no clustering of patients when comparing gene expression in tumor data

## Pathway Activity
1. find more metabolic pathways and compare these genesets and given hallmark genesets by jaccard index
### Pan-cancer analysis
1. z-score (each cancer type) to make the genes comparable
2. GSEA over all genesets for each patient
### KIRC data
1. FC (normal vs cancer data) for every patient
2. GSEA over all genesets for each patient

## **To Do**
1. Finish UMAP on genes for pan-cancer
2. More genesets and Jaccard
3. Run GSEA and plot results
4. generate pathway activity matrices for both data sets based on GSEA results
5. PCA/UMAP on pathway acitvity matrix $\\rightarrow$ clustering?? $\\rightarrow$ e.g. k-means
6. Logistic regression 

**more ideas/possibilities**
1. Look for micro RNA expression/pathways (same principle as for protein coding genes)
2. pathway activity via challenge


##Literature
1. Xiaying Han, Dianwen Song (2022) Using a Machine Learning Approach to Identify Key Biomarkers for Renal Clear Cell Carcinoma
$\\rightarrow$ "However, the main cause of death in KIRC patients is tumor metastasis. There are no obvious clinical features in the early stage of kidney cancer, and 25-30% of patients have already metastasized when they are first diagnosed..."
