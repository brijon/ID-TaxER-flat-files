# ID_TaxER-flat-files

### ID_TaxER_PH_DADA2_Custom_DB.fasta

The custom 16S database for DADA2 </b> allows users to obtain pH classifications for all ASV's generated.This database consists of representative sequences for 13781 dominant OTU's from the 2007 Countryside Survey 16S dataset (consisting of >1000 samples and covering most soil types across Britain). 

The pH classification associated with each representative sequence is based upon hierarchical logistic regression (HOF) models,a series of hierarchical models ranked by their increasing complexity, used to examine taxon responses across ecological gradients.


#### Usage 

Download  <b>ID_TaxER_PH_DADA2_Custom_DB.fasta</b>, and  use as  input for the DADA2 function <b>assignTaxonomy()</b>.
The assignment given to each ASV contains: Countryside survey hit ID, HOF model assigned,pH optima 1,ph optima 2, pH classification & model shape, pH classification, Abundance rank and Occupancy.  

Run as follows:
>assignTaxonomy(seqs,refFasta,taxLevels = c("Countryside survey hit ID", "HOF model assigned","pH optima 1","ph optima 2", "pH classification & model shape", "pH classification", "Abundance rank", "Occupancy"))
 

Refer to https://rdrr.io/bioc/dada2/man/assignTaxonomy.html for further parameter details.




### Additional Information 

This repository is supplementary to the  <b> ID-TaxER (Identification of Taxa & Environmental responses) portal https://shiny-apps.ceh.ac.uk/ID-TaxER/ </b> a shiny interface, enabling users to blast individual sequences against Countryside Survey 16S data to examine the sequences ecological responses and taxonomy.
