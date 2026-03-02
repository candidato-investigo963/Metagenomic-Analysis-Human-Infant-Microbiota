# Metagenomic-Analysis-Human-Infant-Microbiota

# Metagenomic-Analysis-Human-Infant-Microbiota

## Project Overview

This study performs a longitudinal metagenomic analysis based on the ECAM cohort, focusing on the gut microbiota composition of infants at 12 months of age. The research aims to identify microbial variations driven by clinical factors such as delivery mode (Vaginal vs. Cesarean), antibiotic exposure, and sex, while interpreting the biological significance of these shifts in early-life development.The analysis manages the complete bioinformatics workflow, starting from raw sequence import and metadata curation (manifest and mapping files) to advanced differential abundance testing.

The pipeline utilizes the **QIIME2** ecosystem, beginning with a rigorous pre-filtering phase. Sequence quality was validated using **FastQC** and **MultiQC**, consistently showing Phred scores above 30. Denoising was performed via **DADA2** to infer exact Amplicon Sequence Variants (ASVs), achieving retention rates higher than 80% and ensuring a high-fidelity representation of the microbial community over traditional OTU picking.

Data normalization was addressed through rarefaction at a sampling depth of **12,140 reads**, optimized by analyzing alpha rarefaction curves to maximize taxonomic richness while maintaining statistical power across the sample set.

## Diversity and Taxonomic Insights

Statistical analysis of Alpha and Beta diversity revealed that **delivery mode** is the primary driver of microbial community structure. Infants born vaginally exhibited significantly higher richness and evenness (Shannon Index, p=0.002), suggesting a more stable and diverse early colonizing community. Beta diversity metrics, including Bray-Curtis and Jaccard distances (PERMANOVA p=0.02), confirmed distinct clustering patterns based on birth type.

Phylogenetic relationships were established through a *de novo* tree construction (MAFFT and FastTree), allowing for UniFrac distance calculations. Taxonomic classification highlighted a higher prevalence of *Verrucomicrobia* in vaginal births, whereas *Fusobacteria*—often associated with pro-inflammatory states—was more prominent in the cesarean group.

## Differential Abundance and Conclusions

Advanced statistical testing using **ANCOM-BC** identified key biomarkers of gut health. Specifically, *Faecalibacterium prausnitzii* and *Bacteroides uniformis* were significantly depleted in infants born via Cesarean section. These species are well-documented for their beneficial metabolic and immunological roles, suggesting that birth mode may impact long-term health through the initial seeding of the gut ecosystem.




