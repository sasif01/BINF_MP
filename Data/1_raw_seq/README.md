**FASTA and METADATA file**

The FASTA file was too large to include, however, the acesssion numbers for each sequences are in the Meta file

FASTA sequence records for SARS-CoV-2 were retrieved from NCBI Virus. Due to the large number of SARS-CoV-2 sequences available and the limited availability of computing power, it was decided that approximately 2000 sequences were retrieved for each variant across the nine WHO lineages (Alpha, Beta, Epsilon, Eta, Iota, Mu, Omicron, Tau, and Zeta) to ensure fair representation in the dataset. Additional inclusion criteria include the following:
* samples must come from the United States, where sampling efforts remained relatively consistent throughout the pandemic.
* records must contain full-length genomes.
* samples must be from human host.
* records must not contain ambiguous base calls

In addition to the sequence records, the metadata for each lineage and variant were also retrieved, which consisted of the PANGO (Phylogenetic Assignment of Named Global Outbreak) lineage designation and other information (Accession, Release Date, Panoglin, Length, Country, and Collection Date). The PANGO nomenclature is used to classify genetically distinct lineages of SARS-CoV-2, including variants of concern. An additional column was manually added to include the WHO lineage for each variant (e.g., Alpha, Delta, and Omicron). The FASTA sequences and metadata are both necessary for the analyses. Since sequence data was downloaded separately for each variant, Data_organization.script (in the R-Markdown), was created to combine the sequence data into a single file.  

