# Microbiome_Responses_to_Bioinoculants
Here, we explore the potential influence of bacterial inoculants and their associated volatiles on the soil and plant microbiome


**Project Structure**
Fungi_merged.RData: Contains data related to fungal community.
Bacteria_merged.RData: Contains data related to fungal community.
#These data are composed into a phyloseq object

FUNGuild/: Directory containing scripts and tools for functional guild analysis of fungal communities.



Project Structure
Fungi_merged.RData: Contains data related to fungal community.
Bacteria_merged.RData: Contains data related to bacterial community. These data are composed into a phyloseq object.
FUNGuild/: Directory containing scripts and tools for functional guild analysis of fungal communities.
Getting Started
Prerequisites
Python 3.x
R environment
Installation
Clone the repository:

sh
git clone https://github.com/kaboyo/Microbiome_Responses_to_Bioinoculants.git
cd Microbiome_Responses_to_Bioinoculants
Set up Python environment:

sh
conda create --name microbiome python=3.8
conda activate microbiome
Usage
Data Analysis
Prepare your workspace:

sh
cd FUNGuild/
python Guilds_v1.0.py -otu /path/to/otu_table.txt -db fungi
Load and analyze data in R:

R
load("Fungi_merged.RData")
# Perform your analysis
Results
Detailed results and findings are documented in the results/ directory.

Contributors
Your Name
Acknowledgments
This project uses data and tools from the FUNGuild database.
kaboyo/Microbiome_Responses_to_Bioinoculants

