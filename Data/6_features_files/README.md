#AB_content.script

**Purpose**: Determine the AC, GC, AG content of fragments from the referance genome (located in folders inside 5_conserved_seqs/).

**Running the script**: The script is run from command line. The script takes 1 command line arguments (the fragmented referance genome in 
5_conserved_seqs). 

**General format** : python3 AB_content.script frag_ref 
The user will be prompted to specify what base content they want to get (ie, GC or AC or AG)

**4mn_2ovl**

AC content: For loop to get AC content for all files in Data/5_conserved_seqs/4mn_2ovl

`for i in Data/5_conserved_seqs/4mn_2ovl/*; do python3 Code/AB_content.script $i; done`

User input : AC (x15)

AG content: For loop to get AG content for all files in Data/5_conserved_seqs/4mn_2ovl
