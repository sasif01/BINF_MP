**Alignment-MAFFT Results**

Following the pre-processing of the sequence data (2_processed_seqs), sequence alignments were constructed using MAFFT (Katoh and Standley, 2013). Default settings for gap opening and extension penalties were used. 

**Command to run Alignment**

**4mn_2olp**
#Align all Fasta files (located in 2_processed_seqs/4mn_2olp/) in one line using for loop. The resulting aligned files have an .aligned attached their file name

`for i in 2_processed_seqs/4mn_2olp/*; do mafft $i > $i.aligned; done`

**6mn_2olp**
#Align all Fasta files (located in 2_processed_seqs/6mn_2olp/) in one line using for loop. The resulting aligned files have an .aligned attached their file name

`for i in 2_processed_seqs/6mn_2olp/*; do mafft $i > $i.aligned; done`
