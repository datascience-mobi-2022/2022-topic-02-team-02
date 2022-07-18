# Molecular Characterization of Immune Signaling and Metabolic Subtypes in Human Cancer
## A Pan-Cancer Analysis with therapeutic outlooks for clear cell renal cell carcinoma

The aim of this analysis was to determine differences in gene expression and pathway activity in cancer. Fist, pan-cancer analysis was conducted which focuses on 33 different cancer types, and secondly characteristics of kidney renal clear cell carcinoma (KIRC) were investigated in more detail. In the following, the data frame used for pan cancer analysis is referred to as `DF1` and the data set specifically for KIRC as `DF2`. For both data sets, first data cleaning and descriptive analysis were performed. Subsequently, several gene sets have been used to examine pathway activities of the samples more closely: Hallmark, PID and KEGG pathways. Gene set enrichment analysis (GSEA) based on these gene sets was performed to determine enriched pathways. Based on GSEA results differences and similarities between cancer types were analyzed and subtypes were identified by hierarchical clustering. For focused analysis on KIRC, PCA and UMAP allowed identification of sybtypes by k-means. Among others, KIRC subtypes that differ in immune pathway activity could be identified and differences between these subtypes in immune cell fractions were determined using immune deconvolution. Consequently, the subtypes were assigned to high and low immune infiltration. Based on this, a logistic regression was built to predict high or low immune infiltration in KIRC samples, hence to which of the immune subtypes each sample is assigned. 
<br />
<br />

#### Cloning of the repository and data preparation
First, you need to clone the repository using the following link:

git clone <destination> https://github.com/datascience-mobi-2022/2022-topic-02-team-02.git

To run the project, you have to download the following files, including raw and cleaned data, and safe them in the "data" folder:

https://drive.google.com/drive/folders/1O_FXvpRdk7OZJzjisJosr5GLPRRxdUz6

Next, you need to make sure that you can easily access the data. Therefore you will create a new Rstudio project within the repository. This allows accessing all data and files by relative paths. 
<br />
<br />

#### Repository organisation
You will find the analysis divided into several steps, which are organized in the following folders:  

1. Data cleaning <br />
&rarr; Biotype and variance filtering (`DF1`, `DF2`)

2. Descriptive analysis <br />
&rarr; Visualization of data distribution and cleaning steps (`DF1`) <br />
&rarr; Visualization of differential gene expression between normal and tumor tissue(`DF2`)

3. Genesets <br />
&rarr; Comparing genesets using Jaccard index

4. GSEA<br />
&rarr; GSEA (`DF1`, `DF2`) <br />
&rarr; Visualization of pathway activity matrices

5. Dimension reduction <br />
&rarr; PCA (`DF1`, `DF2`) and UMAP (`DF1`)

6. Clustering <br />
&rarr; Hierarchial clustering on PID geneset (`DF1`) <br />
&rarr; K-means clustering on Hallmark, PID, KEGG and all combined gene sets and comparison of PID and KEGG subtypes (`DF2`)

7. Immune deconvolution <br />
&rarr; Determination of immune cell fractions in KIRC (`DF1`, `DF2`)

8. Logistic regression <br />
&rarr; Predicting high or low immune infiltration of KIRC samples

9. Figures <br />
&rarr; Final version of figures used in the report



