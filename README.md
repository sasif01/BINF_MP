# BINF*6999 Master Project in Bioinformatics
Masters Project in Bioinformatics - analyzes drift resistant regions of vial genomes 

Folders Code/ and Data/ contain the scripts and sequences for the project

**Workflow**

Pipeline Overview


Metadata from the sequence records are used in a python script to filter the sequences in the fasta based on WHO lineage and variant (variant_timeframes.script) (Figure 1. B). The resulting FASTA files for each lineage and variant are aligned using MAFFT (Katoh and Standley, 2013) and the consensus sequences are generating in R (Figure 1. C). Conserved regions are determined using the consensus sequences to measure the stability of the fragment’s relative others across the genome (Figure 1. D). From stable regions of the sequences, information is extracted using python script feature.script (Figure 1. E). The results are used to predict the stability of candidate target regions across other respiratory viruses. 

**Code/**: Contains the python/R scripts 

**Script 1 (vairent_timeframes.script)**: First script to run.

Running the script:The script takes user input and 2 command line arguments (first = Meta file, second = Fasta file, both are 
located in the Data/raw_seq/ folder).
	
Purpose: Reorganizes the sequences in the fasta file. For WHO Lineages (WHO lineages: Alpha, Delta, Omicron etc.) with multiple 
variants (ie. Omicron), the sequences are separated by variant. WHO lineages with a single variant (Alpha, Beta etc.) are 
separated into fixed time intervals (in months), with a given overlap between intervals, specified by the user.
	
Results: The output is multiple fasta files names after the Lineage and varient or the Lineage and time-interval. The fasta files are in the Data/processed_seqs/ folder.
	
**Alignment-MAFFT**: Fallowing the organization of the sequences, alignments for each grouping are constructed using MAFFT. The command to run alignments on all the fasta files at once is in the R-Markdown for the project. 
	
Results: The resulting files are found in the Data/aligned_seqs/ folder

**Consensus-R**: Generates a consensus sequences using the aligned files from each varient/time-interval. The ConsensusSequence() is used. The values of the threshold can be adjusted to alter the sequences represented in the consensus. 
	
Results: A fasta file containing all the consesnsus sequences is produced. Multiple files can be generated for a aligned files by altering the threshold parameter in the ConsensusSequence() function. The files are in Data/consensus_seqs/

**Script 2** (conservation_score.script): The script takes one command line argument (the consensus sequences file) and user input.
	
Purpose: Score each base in of the consensus sequnces based on if the same base is present in the referance Sars-CoV-2 sequence or in the aligned sequences files. Fragment the consensus (length of fragment is specified by user) and filter out segments that have an average score lower then the one specified by the user. The resulting fragment are considered highly stable.
		
Results: For each consensus sequences (which are all in a single file), a fasta containing the 'highly stable' fragments is generated, with the lineage, varient, and location (in the consensus genome) information. The files are located in the Data/fragmented_seqs


<img width="574" alt="Screenshot 2023-08-14 at 11 27 06 AM" src="https://github.com/sasif01/BINF_MP/assets/114173014/55b21ae2-ec67-4b84-b823-e15a6bf7f0a4">

