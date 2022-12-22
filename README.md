# single_marker_gene_microbiome_analysis
Repository to hold analysis for single marker genes in HNSC Microbiome

* Look at 16S and rpob dnak genes, especially the single copy genes - rpoB has the most literature
* Add any paper links to this repoistory

http://frogs.toulouse.inra.fr 

Bioinformatics Ideas
1. Create a list genera/species known to be in the HNSC microbiome (in progress). Err on the side of completeness
* eHOMD database for human oral microbiome database
* GTDB identification/Silva identification/ Actual name we want (species name) - big spreadsheet
2. Pull all sequences from GTDB https://gtdb.ecogenomic.org especially dnak and rpoB gene - MLST typing probably helpful here
* To be done - how to actually get 16S from Silva https://www.arb-silva.de and rpoB genes from GTDB
* shell scripts to do this (gtdb has own program I think)
* Hard part - getting rpob genes. Will likely involve prokka -> extraction of gene. Might create my own program eventually see below
* Should be handled with snakemake (George) when actually run, but for now, Kenny figure out how to do it on 1 sample (python).
3. Create multiple sequence alignment (MAFFT/PRANK) of the genes and idenity regions that are conserved
* Very easy once this 2 is done.
4. Create primers - LOGO to do this

Other ideas (George)
* Try to apply phylomagnet to TCGA
* rpob gene extraction program? like barrnap

Other notes from Meeting with Przemeck

* 5-8 nts at the 3' end are the most important and must be there to amplify
* Likely to use EUPA code (ambiguity in some spots of primer)
* Consider orthoANIu instead of FastANI as it gives coverage
* SRA search for other WGS databasets
* Search for antibiotics in the MAGs


Other literatue

* https://bmcmicrobiol.biomedcentral.com/articles/10.1186/s12866-019-1546-z
* https://www.mdpi.com/2073-4425/11/2/139/htm

# Plan

* Everything saved as shell scripts in this directory for now in this directory (.sh files)
* Do not upload genomes (too big)
