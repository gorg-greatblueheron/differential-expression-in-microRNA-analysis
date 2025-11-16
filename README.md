Differential Expression of Circulating microRNAs in Sickle Cell Disease

Background: 
Sickle Cell disease (SCD) is an inheritable genetic disease disorder, with an elevated risk for chronic kidney disease, pulmonary embolisms, exertional rhabdomyolysis. 
The burden of the SCD affect 8 million people worldwide, especially non-Hispanic black or African American population.
Overview: 
This project analyzes circulating microRNA across three sickle cell disease (SCD) genotypes - HbAA(control), HbAS(carrier), and HbSS(diseased) - using high thoroughput sequencing data from the University Of Texas Southwestern Medical Center. 
The goal is to identify differentially expressed microRNA associated with genotype and to visualize patterns using volcano plots and heatmaps. 

Dataset
Source: UT Southwestern Medical Center
Samples: Plasma samples from self-identified black race human subjects with HbAS, HbSS, HbAA selected from the Mass General Brigham Biobank. HbAA were matched to HbAS(1:1) and HbSS(1:3) based on age, sex, and eGFR. The total sample size is 39. 
Website: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE285580

Method: 
Data has already been pre-processed and normalized prior to analysis. 
Differential expression analysis was performed using the linear model for microarray package. Volcano plots were generated to visualize the results of differential expression analysis between genotype groups.
miRNA were plotted with log2 Fold change on x-axis and p value on y-axis. Statistical significance was defined as an adjusted p value (p < 0.05). Points were colored based on this threhold using ggplot in R. 
Heatmap were generated to visualize the expression patterns of top differentially expressed miRNA across genotype groups. Top 20 miRNAs were selected based on adjusted p values, sorted by false recovery rate (FDR). 
Functional enrichment analysis was performed to identify biological process that are over-represented among the expressed miRNAs. Special attention was given to gene ontology (GO) terms related to immune function. 
Statistical enrichment strength was determined/visualized using bar chart. 


Key results: 
None of the individual observation of miRNA pass the significant threhold (FDR < 0.05). A small number of miRNA exhibited the large fold changes but did not reach statistical significance.
However, the heatmap have cleared revealed a subset of approximately 6-8 miRNA that were relatively overexpressed in HbSS samples. These miRNA appear as brighter (red-shaded) rows in several HbSS columns, whereas same miRNA showed more neutral/lower expression levels in HbAS/HbAA samples
Functional enrichment analysis determined that top significant GO terms were related to neuronal/axonal pathways, intracelluar transport/organization, signal transduction via GTP-ases, and macroautophagy (closely related to inflammatory regulation)


Repository structure: 



Requirements: 
R (>=4.2.0)
Key packages: tidyverse, DESeq2, pheatmap, ggplot2

