### MS biology — the disease you'd be studying

What is MS:
Multiple sclerosis is an autoimmune disease where the immune system attacks myelin (the insulation around nerve fibres) in the brain and spinal cord. It's driven by autoreactive T cells and B cells that cross the blood-brain barrier.

##### Key cell types in MS:

CD4+ Th17 cells    → main drivers of inflammation
CD8+ cytotoxic T   → directly kill oligodendrocytes
B cells / plasmablasts → produce antibodies, antigen presentation
Regulatory T cells → failing to suppress autoimmunity
Microglia          → brain-resident macrophages, "smoldering" inflammation

"Smoldering MS" — the focus of this position — 
refers to chronic, low-grade inflammation that continues even when relapses are controlled by treatment. 
brain-residing antibody-secreting cells in MS, suggesting B cells that hide in the brain drive this smoldering activity.

Papers to read immediately:

##### Kappos et al. 2020 Nature — smoldering MS concept
##### Absinta et al. 2021 Nature Medicine — chronic active lesions
##### Hauser et al. 2017 NEJM — B cells in MS (ocrelizumab trial)


**Multi-omics data integration — the core technical skill**

Van de Werken's group has dedicated workflows for Whole Genome Sequencing, Whole Exome Sequencing, ChIP-seq, Chromatin Conformation Capture, mRNA-seq, small RNA-seq, DNA methylation, RNA-seq and Proteomics integration. You'd be working alongside this infrastructure.

What you need to learn:

r
##### Key packages for multi-omics integration
BiocManager::install("MultiAssayExperiment")  # store multiple data types per patient
install.packages("mixOmics")                  # DIABLO — multi-omics integration
BiocManager::install("MOFA2")                 # Factor analysis across modalities

##### For genetic data (GWAS)
install.packages("TwoSampleMR")     # Mendelian randomisation
install.packages("coloc")           # colocalisation of GWAS + eQTL signals
BiocManager::install("SNPRelate")   # genetic data processing

The key concept — patient as the unit of integration:

Patient A:
  - RNA-seq of blood T cells
  - Serology (antibody levels against EBV, VZV)
  - MRI lesion count
  - Genetic variants (HLA type, MS risk SNPs)
  - Clinical: EDSS score, relapse rate, treatment

Your job: find computational signatures that predict disease progression


**Neuroimmunology-specific data types**

Cerebrospinal fluid (CSF) analysis — unique to neurological diseases:

Oligoclonal bands (OCBs) — IgG bands in CSF = B cell activation in CNS
CSF cell count and composition
Intrathecal antibody production

##### How to analyse it computationally:

r
###### CSF immune cell profiling with scRNA-seq
###### Same Seurat pipeline but different cell type expectations:
###### - T cells, B cells, monocytes, plasma cells



###### - Look for: clonally expanded B cells, exhausted T cells
###### - Compare CSF vs blood from same patient (paired analysis)


############################################

### MS biology

Read 5 key MS papers (list below)
Understand the clinical data: EDSS, MRI lesion types, treatment response
Learn what "smoldering MS" means biologically

##### Dendrou et al. 2015 Nature Reviews Immunology — "Immunopathology of multiple sclerosis" — start here, best overview
##### Absinta et al. 2021 Nature Medicine — smoldering lesions, directly relevant to the position
##### Schirmer et al. 2019 Nature — scRNA-seq of MS brain lesions
##### Ramaglia et al. 2023 — NIB group paper on B cells in MS brain
##### International MS Genetics Consortium 2019 Science — GWAS of 47,000 MS patients

### multi-omics integration

Learn MOFA2 (you already have it as a skill in your profile)
Practice integrating RNA + clinical data on a public MS dataset
Dataset: GEO GSE138266 (scRNA-seq of MS patient blood)

### genetics

Learn what GWAS output looks like and how to read it
Learn about HLA typing (critical for MS — HLA-DRB1*15:01 is the biggest MS risk gene)
Practice with the IMSGC GWAS data (publicly available)
