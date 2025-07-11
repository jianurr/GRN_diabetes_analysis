#  Gene Regulatory Network Analysis of Diabetes Dataset

A bioinformatics project focused on reconstructing and analyzing a Gene Regulatory Network (GRN) using real gene expression data related to *diabetes mellitus**.

---

##  Objectives:

-  Download and preprocess gene expression data from NCBI-GEO
-  Construct the Gene Regulatory Network using the ARACNE algorithm
-  Visualize and analyze the network using Cytoscape
-  Study topological features including clustering, centrality, and scale-free behavior

---

##  Dataset Information

- * Source*: [NCBI GEO: GSE290271](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE290271)  
- * Type*: Processed RNA-Seq FPKM values  
- * Description*: Dataset from study involving diabetes and ferroptosis-related gene expression  
- * File Used*: GSE290271_Genes_fpkm.csv

---

##  Tools & Technologies

| Tool/Software | Purpose                                |
|---------------|----------------------------------------|
| *R / RStudio*      | GRN construction using ARACNE         |
| *Cytoscape*        | Network visualization and analysis    |
| *R (powerlaw)*     | Power-law and scale-free property fit |
| *GitHub*           | Project version control               |

---

##Project Structure
GRN_Diabetes_Analysis/
├── dataset/               # Gene expression data
├── R scripts/               # R scripts for GRN and power-law analysis
├── cytoscape results/       # Network edge list and visualization files
├── results/               # Output from R
└── README.md              # Project overview and documentation

##  Topological Properties (Summary)

| Property                    | Value       |
|----------------------------|-------------|
| Nodes                      | 100         |
| Edges                      | 296         |
| Avg. Neighbors             | 2.96        |
| Clustering Coefficient     | 0.042       |
| Diameter                   | 11          |
| Path Length (Characteristic) | 4.875     |
| Network Centralization     | 0.031       |
| Power-law Exponent (α)     | 7.34        |
| Xmin                       | 8           |

> ⚠ *Note: Power-law exponent > 3 suggests **weak scale-free behavior*, which is not typical for biological GRNs.

---

##  Key Findings

- Hub genes: *Smc3, **Actr1a, **Dpcd, **Wls, **Zdhhc6*
- Network does *not strongly follow scale-free topology*
- Centrality and clustering metrics indicate moderately connected structure

---

<details>
<summary> How to Reproduce the Analysis</summary>

1. *Download Data*
   - From [GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE290271)
   - Use processed .csv FPKM data

2. *Construct GRN*
   - Run scripts/GRN_ARACNE.R in R
   - Export edge list as GRN_edges.csv

3. *Visualize & Analyze in Cytoscape*
   - Import the CSV using File → Import → Network from File
   - Go to Tools → Analyze Network for metrics

4. *Power-law Analysis*
   - Run scripts/powerlaw_analysis.R to fit and evaluate degree distribution
</details>

---

##  Author

**Khandakar Jianur Islam 
M.Sc. Bioinformatics  
Jamia Millia Islamia**
