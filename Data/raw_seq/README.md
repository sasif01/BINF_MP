FASTA and METADATA file 


Data is retrieved from NCBI Virus. For each lineage of Sars-CoV-2, up to approximately 2000 sequences are retrieved per variant 
to ensure accurate representation in the dataset. The data is filtered to include only samples from the United States, where 
sampling efforts remained relatively consistent throughout the pandemic. Additionally, only full-length genomes samples and 
samples from human host were retained. Furthermore, the maximum number of ambiguous characters were limited to 0 for each 
sequence to ensure the consensus are more accurate. Lastly, the metadata files for each lineage and variant are retrieved, 
which consists of the pango lineage designation and other filter information (Accession, Release Date, Panoglin, Length, 
Country, Collection Date). An addition column is added to each table to include the WHO lineage for each variant (ie. Alpha, 
Delta, Omicron, etc.). The Fasta sequence file and the metadata file are both necessary for the analyses.  Since sequence data 
was downloaded separately for each variant, additional steps, which are outlined in the Markdown file, are taken to combine the 
raw data into a single file. 
