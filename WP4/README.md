## Outline of WP4 workflows

### 1. Metabarcoding
Analysis of metabarcoded sequences (16S/ITS) is done using [a version of the SimpleMetaPipeline that is optimised for PacBio sequences.](https://github.com/Microbiome-Revolution/SimpleMetaPipeline) 

<img src="https://github.com/Microbiome-Revolution/Data-standard/blob/main/WP4/SimpleMetaPipeline_Workflow.png" alt="Graphical abstract of SimpleMetaPipeline" width="400"/>

This generates *2* main result files and *7* post-run diagnostic files as outlined in [section 4.2 of the SimpleMetaPipeline repository](https://github.com/Microbiome-Revolution/SimpleMetaPipeline?tab=readme-ov-file#42-inspecting-the-example-intermediateoutputs-and-results)

The output file that is passed on to the other WPs has the suffix "*_SeqDataTable.csv"
Table headers are defined in [SeqDataTable_metadata.md](https://github.com/Microbiome-Revolution/Data-standard/blob/main/WP4/SeqDataTable_metadata.md)

### 2. Bacterial Metagenomics
Analysis of metagenomic sequencing reads is done using pipeline for Upscaled Resolution of Ecological Networks (UREN)

<img src="https://github.com/Microbiome-Revolution/Data-standard/blob/main/WP4/mtg.jpg" width="1000"/>

### 3. Viral Metagenomics
Analysis of viral sequencing reads is done using the pipeline for [ insert querky virus pipeline name ] 

<img src="https://github.com/Microbiome-Revolution/Data-standard/blob/main/WP4/vir_mtg.jpg" width="1000"/>
