**Stability Scores**

Using the consensus sequences (from the folders in Data/4_consensus_seqs/), the referance genome (NC_045512.2) is scored based on number 
of bases that are common across the referance and the consensus sequences. The referance genome is then fragmented into >100base pairs 
lengths across the entire sequence.  The choice is because a PCR-based detection assay typically requires a region of around 100 or more 
base. The results 
 

Script 2 (variant_conservation.script) is used to score and fragment the referance. 

**Running the script** (From BINF_MP) :

**4mn_2ovl**

#For loop to score and fragment  each of the five consensus files in this folder.

`for i in Data/4_consensus_seqs/4mn_ovlp/*; do python3 Code/variant_conservation.script $i Data/referance.fasta; done`

#The user will need to specify the length of the fragments for each file. 
User input setting: Length of fragment: 100 (x5) 

This is done 3 times, to get files with the referance fragmented into 100bp, 150bp and 200bp


**6mn_olp**

The same is done for the fils in the  Data/4_consensus_seqs/6mn_olp/ folder.

#For loop to score and fragment  each of the five consensus files in this folder.

`for i in Data/4_consensus_seqs/6mn_olp/*; do python3 Code/variant_conservation.script $i Data/referance.fasta; done`

#The user will need to specify the length of the fragments for each file.
User input setting: Length of fragment: 100 or 150 or 200 (x5)

This is done 3 times, to get files with the referance fragmented into 100bp, 150bp and 200bp


