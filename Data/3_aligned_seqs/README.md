**Alignment-MAFFT Results**

Following the pre-processing of the sequence data (2_processed_seqs), sequence alignments were constructed using MAFFT (Katoh and Standley, 2013). Default settings for gap opening and extension penalties were used. 

**Command to run Alignment**

#Align all Fasta files (located in 2_processed_seqs/) in one line using for loop. The resulting aligned files have an .aligned attached their file name

`for i in 2_processed_seqs/*; do mafft $i > $i.aligned; done`
