# Unsere Überschrift 

The aim of this analysis was to determine differences in gene expression and pathway activity in cancer. Fist, pan-cancer analysis was conducted which focuses on 33 different cancer types, and secondly characteristics of kidney renal clear cell carcinoma (KIRC) were investigated in more detail. In the following, the data frame used for pan cancer analysis is referred to as "DF1" and the data set specifically for KIRC as "DF2". For both data sets, fist data cleaning and descriptive analysis were performed. Subsequently, several genesets have been used to examine pathway activities of the samples more closely: Hallmark, PID, KEGG, PENG and MMR pathways. Gene set enrichment analysis (GSEA) based on these genesets was performed to determine enriched pathways. Based on GSEA results differences and similarities between cancer types were analyzed and subtypes were identified by hierarchical clustering. For focused analysis on KIRC, PCA and UMAP allowed identification of sybtypes by k-means. Among others, KIRC subtypes that differ in immune pathway activity could be identified and differences between these subtypes in immune cell fractions were determined using immune deconvolution. Consequently, the subtypes were assigned to high and low immune infiltration. Based on this, a logistic regression was built to predict high or low immune infiltration in KIRC samples, hence to which of the immune subtypes each sample is assigned. 
<br />
<br />

#### Cloning of the repository and data preparation
First, you need to clone the repository using the following link:

**link**

To run the project, you have to download the following files, including raw and cleaned data, and safe them in the "data" folder:

**link**

Next, you need to make sure that you can easily access the data. Therefore you will create a new Rstudio project within the repository. This allows accessing all data and files by relative paths. 
<br />
<br />

#### Repository organisation
You will find the analysis divided into several steps, which are organized in the following folders:  

1. Data cleaning <br />
$\\rightarrow$ Data cleaning (DF1, DF2): biotype and variance filtering

2. Descriptive analysis <br />
$\\rightarrow$ Visualization of data distribution and cleaning steps (DF1) <br />
$\\rightarrow$ Visualization of differential gene expression between normal and tumor tissue(DF2)

3. Dimension reduction <br />
$\\rightarrow$ PCA (DF1, DF2) and UMAP (DF1)

4. Genesets <br />
$\\rightarrow$ Comparing genesets using Jaccard index

5. GSEA<br />
$\\rightarrow$ GSEA (DF1, DF2) <br />
$\\rightarrow$ Visualization of pathway activity matrices

6. Clustering <br />
$\\rightarrow$ Hierarchial clustering on PID geneset (DF1) <br />
$\\rightarrow$ K-means clustering on Hallmark, PID, KEGG and all combined genesets and comparison of PID and KEGG subtypes (DF2)

7. Immune deconvolution <br />
$\\rightarrow$ Determination of immune cell fractions in KIRC (DF1, DF2)

8. Logistic regression <br />
$\\rightarrow$ Predicting high or low immune infiltration of KIRC samples



