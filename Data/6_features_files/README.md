# AC_content, AG_content, GC_content

**AB_content.script**

**Purpose**: Determine the AC, GC, AG content of fragments from the referance genome (located in folders inside 5_conserved_seqs/).

**Running the script**: The script is run from command line. The script takes 1 command line arguments (the fragmented referance genome in 
5_conserved_seqs). 

**General format** : python3 AB_content.script frag_ref 
The user will be prompted to specify what base content they want to get (ie, GC or AC or AG)

**4mn_2ovl**

AB content: For loop to get AB content for all files in Data/5_conserved_seqs/4mn_2ovl

`for i in Data/5_conserved_seqs/4mn_2ovl/*; do python3 Code/AB_content.script $i; done`

User input : AC or AG or GC (x15)

**6mn_2ovl**
`for i in Data/5_conserved_seqs/6mn_2ovl/*; do python3 Code/AB_content.script $i; done`

User input :  AC or AG or GC (x15)


# genome_location
**genome_location.script**
**Purpose** : To determine the location of conserved/non-conserved fragments of the reference genome (located in folders inside 5_conserved_seqs/). The reference genome is sectioned into 4 quarters and fragments (from files in folders of 5_conserved_seqs) are labeled accordingly. 

**Results/Output** : The result/output for genome_location.script is a 
 








