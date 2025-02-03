# Microbiome_Responses_to_Bioinoculants
Here, we explore the potential influence of bacterial inoculants and their associated volatiles on the soil and plant microbiome

**Raw data for reproducing this analysis is deposited on https://www.ebi.ac.uk/ena/browser/view/PRJEB61122; downloaded using SRA-tools**

**Project Structure**
The object:
Fungi_merged.RData — Contains data related to the fungal community.
Bacteria_merged.RData — Contains data related to bacterial commmunity community.
**These data are composed into phyloseq formated objects**
The objects are composed from the files metadata, asv/formerly called OTU table, and the taxonomy tables for bacterial and fungal community, respectively: 
-Mapping_File_16S_Combined.txt
-Bacteria-table.txt
-Taxon_Bacteria.txt
&
-Mapping_File_ITS_Combined.txt
-Fungi-table.txt
-Taxon_Fungi.txt

**Microcosm.Rmd — R script used to load processed microbiome data**

**Functional assignment of community was based on scripts defined for bacterial and fungal community functional assignment, present in:**
-FUNGuild/: Directory containing scripts and tools for functional guild analysis of fungal communities.
-FAPROTAX_1.2.10/: Directory containing scripts and tools for functional guild analysis of bacterial communities.


**Getting Started**
Prerequisites
Python 3.x
R environment

**Installation**

1. Clone the repository:

```
sh
git clone https://github.com/kaboyo/Microbiome_Responses_to_Bioinoculants.git
cd Microbiome_Responses_to_Bioinoculants
```

Set up Python environment:

```
sh
conda create --name microbiome python=3.8
conda activate microbiome
```

**Usage**

**Data Analysis*
#Functinal predictions**
Prepare your workspace:

```
sh
cd FUNGuild/
python Guilds_v1.0.py -otu /path/to/otu_table.txt -db fungi
```
```
sh
cd FAPROTAX_1.2.10/
./collapse_table.py -i otu_table.biom -o functional_table.biom -g FAPROTAX.txt
```

# Perform your analysis using the Rscript by loading the script in R:
#Note to define the right directory

```
Microcosm.Rmd
```
#Fungal community
```
R
load("Fungi_merged.RData")
```

#Bacterial community
```
R
load("Bacteria_merged.RData")
```

Contributors
Expedito Olimi
Acknowledgments
This work was supported by the EXCALIBUR research project with funding from the European Union’s Horizon 2020 Research and Innovation Program under grant agreement No. 817946 (to Gabriele Berg).![image](https://github.com/user-attachments/assets/5e3cce01-f2d7-4d79-9935-d7fa93e77d34)



