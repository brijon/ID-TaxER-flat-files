# ID_TaxER-Custom-Database-for-DADA2 

<b>Description</b>

This repository provides a custom 16S database for DADA2 allowing users to obtain pH classifications for all ASV's generated.This database consists of representative sequences for 14495 dominant OTU's from the 2007 16S Countryside Survey dataset (consisting of 1000 samples and covering most soil types across the Uk). 

The pH classification associated with each representative sequence is based upon hierarchical logistic regression (HOF) models,a series of hierarchical models ranked by their increasing complexity, used to examine taxon responses across ecological gradients.




<b>Usage</b>

Download  <b>ID_TaxER_PH_DADA2_Custom_DB.fasta</b>, and  use as  input for the DADA2 function <b>assignTaxonomy(),</b>.
The assignment given to each ASV contains: Countryside survey hit ID, HOF model assigned, pH classification based on model optima, pH classification & model shape, and one or two model optima depending on model type.  

<b> Additional Information </b>

This DADA2 custom database supplements the  ID-TaxER (Identification of Taxa & Environmental responses) portal https://shiny-prod.nerc-lancaster.ac.uk:8443/brijon/Trait-matrix/ a shiny interface, enabling user's to blast individual sequences against 16S Countryside Survey data to examine the sequences ecological responses and taxonomy.
