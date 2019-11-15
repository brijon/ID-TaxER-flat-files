# ID_TaxER-flat-files



### Summary

This repository is supplementary to the  <b> ID-TaxER (Identification of Taxa & Environmental responses) portal https://shiny-apps.ceh.ac.uk/ID-TaxER/ </b> a shiny interface, enabling users to blast individual sequences against Countryside Survey 16S data to examine the sequences ecological responses and taxonomy.

The database consists of 13781 OTU's from the 2007 Countryside Survey 16S dataset, consisting of >1000 samples and covering most soil types across Britain. All pH classifications of OTU’s are based upon hierarchical logistic regression (HOF) models, a series of hierarchical models ranked by their increasing complexity, used to examine taxon responses across ecological gradients.


This repository contains a number of flat files enabling batch querying of the ID-TaxER database; please see below for full descriptions of each file. 

### HOF_model_features.csv
A CSV file containing the following for all 13781 OTU's: HOF model assigned, pH optima 1, ph optima 2, pH classification & model shape, pH classification, Abundance rank, Occupancy.


### ID_TaxER_PH_DADA2_Custom_DB.fasta

A custom 16S database for DADA2 allowing the user to obtain pH classifications for all ASV's generated. 

This database was created to be used with the DADA2 function <b>assignTaxonomy()</b>.
The assignment given to each ASV contains: Countryside survey hit ID, HOF model assigned,pH optima 1,ph optima 2, pH classification & model shape, pH classification, Abundance rank and Occupancy.  

Run as follows in R:
>assignTaxonomy(seqs,refFasta,taxLevels = c("Countryside survey hit ID", "HOF model assigned","pH optima 1","ph optima 2", "pH classification & model shape", "pH classification", "Abundance rank", "Occupancy"))
 

Refer to https://rdrr.io/bioc/dada2/man/assignTaxonomy.html for further parameter details.

### repseqs.fasta

A unannotated fasta file of all 13781 OTU representative sequences.

### taxonomy.csv

A CSV file containing taxonomic annotation for all 13781 OTU's.

### user_data_upload.csv

A CSV template for submitting new “trait” information to existing ID-TaxER OTU’s. Please send submissions to rig@ceh.ac.uk.

