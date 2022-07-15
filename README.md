# Unsere Überschrift 

The aim of this analysis was to determine differences in gene expression and pathway activity in cancer. Fist, pan-cancer analysis was conducted which focuses on 33 different cancer types, and secondly characteristics of kidney renal clear cell carcinoma (KIRC) were investigated in more detail. In the following, the data frame used for pan cancer analysis is referred to as "DF1" and the data set specifically for KIRC as "DF2". For both data sets, fist data cleaning and descriptive analysis were performed. Subsequently, several genesets have been used to examine pathway activities of the samples more closely: Hallmark, PID, KEGG, PENG and MMR pathways. Gene set enrichment analysis (GSEA) based on these genesets was performed to determine enriched pathways. Based on GSEA results differences and similarities between cancer types were analyzed and subtypes were identified by hierarchical clustering. For focused analysis on KIRC, PCA and UMAP allowed identification of sybtypes by k-means. Among others, KIRC subtypes that differ in immune pathway activity could be identified and differences between these subtypes in immune cell fractions were determined using immune deconvolution. Consequently, the subtypes were assigned to high and low immune infiltration. Based on this, a logistic regression was built to predict high or low immune infiltration in KIRC samples, hence to which of the immune subtypes each sample is assigned. 

## Clone the repository
To run the project, you need to download the following files, including raw and cleaned data, and safe them in the "data" folder:

You will find the analysis divided into several steps, which are organized in the following folders:  

1. Data cleaning 

$\\rightarrow$ Data cleaning for DF1 and DF2: Biotype and variance filtering

2. Descriptive analysis

$\\rightarrow$ Visualization of data distribution and cleaning steps for DF1
$\\rightarrow$ Visualization of differential gene expression between normal and tumor tissue (DF2)

3. Dimension reduction

$\\rightarrow$ PCA (DFF1, DF2) and UMAP (DF1)

4. GSEA

$\\rightarrow$ GSEA for DF1 and DF2
$\\rightarrow$ Visualization of pathway activity matrices

5. Clustering

$\\rightarrow$ DF1: Hierarchial clustering on PID geneset
$\\rightarrow$ DF2: K-means clustering on Hallmark, PID, KEGG and all combined genesets and comparison of PID and KEGG subtypes

6. Immune deconvolution

$\\rightarrow$ Determination of immune cell fractions in KIRC (DF1 and DF2)

7. Logistic regression

$\\rightarrow$ Predicting high or low immune infiltration of KIRC samples








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


