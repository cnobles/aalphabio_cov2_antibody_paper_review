# Review of A-Alpha Bio Manuscript on Affinity Characterization of Antibodies against SARS-CoV-2 Variants

## Resource Links:
* [Manuscript](https://doi.org/10.1101/2021.04.27.440939)
* [Code Repository](https://github.com/A-AlphaBio/cov2_antibodies_variants)
* [AlphaSeq Assay Manuscript](https://pubmed.ncbi.nlm.nih.gov/29087945/)

## Manuscript Summary:
Antibody therapies are a valuble tool in reducing COVID-19 deaths and hospitalizations, the disease is caused by the SARS-CoV-2 virus. Viral entry into cells involves the viral Spike protein binding to the host ACE2 receptor through the spike protein's recepter binding domain (RBD). The RBD has been the target of therapeutic antibody targeting for this reason. Several SARS-CoV-2 strains have mutations in the RBD which increase ACE2 binding affinity, effectively increasing viral transmission and escape from existing antibody therapies. This manuscript uses a yeast synthetic agglutination assay to massively parallelize the screening of 33 antibodies against variations of the RBD to predict binding strength and identify clinically significant residues that may influence antibody binding, suggesting how future RBD variants may impact antibody therapies effectiveness.

Using the AlphaSeq assay, the authors were able to measure over 170,000 different protein-protein interactions (PPIs) using clinically significant antibodies against RBD variants. While one other assay was able to measure affinies against RBD variants (Starr et al.), the assay lacked throughput and could only be done on a single antibody at a time. In the AlphaSeq experiment, the authors were able to evaluate 33 therapeutically relevant antibodies against most single-amino-acid mutations in the SARS-CoV-2 Spike RBD, as well as widely circulating multiple mutation variants. 

In the first AlphaSeq experiment, the 33 antibodies were screened against a site-saturation mutagenesis library of the Spike RBD, representing approximately 75% of all single residue mutants across the 165 amino-acid positions. By measuring the representation in a pairwise manner (between antibody and RBD site barcodes), the AlphaSeq assay produced an estimation of the interaction affinity. Reviewing the data revealed sites with significant decreased in antibody affinity when changed to different residues. These sites were notably marked as locations of antibody binding, and corroborate findings from other research. Knowing the impact on affinity from changing single residues in the RBD could provide a prediction for when variants arise in those regions naturally.

In a second AlphaSeq experiment, the 33 antibodies and ACE2 were screened against 34 SARS-CoV-2 RBD variants with single, double, or triple mutations and included 5 CDC-defined variants of concern (B.1.1.7, B.1.351, P.1, B.1.427, and B.1.429). While a smaller scope for measuring PPIs, the experiment provides some interesting and highly relevant information. The majority of mutations in the RBD lead to stronger binding to viral entry receptor ACE2 (supported by other research) and decreased the binding toward therapeutic antibodies. In this same experiement, other coronavirus spike protein RBDs were included to test for specificity of antibodies, revealing that several clinically relevant antibodies were cross-reactive with other coronaviruses, including SARS-CoV-1, LYRa11, WIV1, and RaTG13. 

## Goals of Review
The following are goals of this review:
1. Read and summarise the manuscript, download and review the associated data (present in /manuscript_data), and review binding data for epitote discovery.
2. Find antibodies from the manuscript with bound structures available in the PDB, annotate which antigen residues are within 4 Angstroms, and compare these results with those reported in the manuscript.
3. Using the AlphaSeq data from the manuscript, implement and benchmark an epitope-calling algorithm (raw data present in table 4 of supplementary info).

## Notes:
1. PDB search options often return unrelated structures or multiple structures have been submitted matching the query ("antibody identifier" + "SARS-CoV-2"). In the case of multiple structures, finer resolution structures were prefered and only one structure was selected per CoV binder.