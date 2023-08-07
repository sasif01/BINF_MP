# BINF*6999 Master Project in Bioinformatics
Masters Project in Bioinformatics - analyzes drift resistant regions of vial genomes 

Folders Code/ and Data/ contain the scripts and sequences for the project

**Workflow**

Code/: Contains the python/R scripts 

*Script 1 (vairent_timeframes.script): First script to run. Takes user input and 2 command line arguments (first = fasta 
file, second = meta file, both are located in the Data/raw_seq/ folder). 
	Purpose: Reorganizes the sequences in the fasta file. For Lineages (ie. WHO lineages: Alpha, Delta, Omicron) with 
multiple varients (ie. Omicron), the sequences are seperated by varient. WHO lineages with a single varient (ie. Alpha) are 
separated into fixed time intervals (in months), with a given overlap between intervals, specified by the user. 
	Results: The output is multiple fasta files names after the Lineage and varient or the Lineage and time-interval. The 
fasta files are in the Data/processed_seqs/ folder.
	
*Alignment-MAFFT: Fallowing the organization of the sequences, alignments for each grouping are constructed using MAFFT. The 
command to run alignments on all the fasta files at once is in the R-Markdown for the project. 
	Results: The resulting files are found in the Data/aligned_seqs/ folder

*Consensus-R: Generates a consensus sequences using the aligned files from each varient/time-interval. The ConsensusSequence() 
is used. The values of the threshold can be adjusted to alter the sequences represented in the consensus. 
	Results: A fasta file containing all the consesnsus sequences is produced. Multiple files can be generated for a 
aligned files by altering the threshold parameter in the ConsensusSequence() function. The files are in Data/consensus_seqs/

*Script 2 (conservation_score.script): The script takes one command line argument (the consensus sequences file) and user 
input.
	Purpose: Score each base in of the consensus sequnces based on if the same base is present in the referance Sars-CoV-2 
sequence or in the aligned sequences files. Fragment the consensus (length of fragment is specified by user) and filter out 
segments that have an average score lower then the one specified by the user. The resulting fragment are considered highly 
stable.
	Results: For each consensus sequences (which are all in a single file), a fasta containing the 'highly stable' 
fragments is generated, with the lineage, varient, and location (in the consensus genome) information. The files are located in 
the Data/fragmented_seqs



