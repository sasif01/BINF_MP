1_raw_seqs : First folder. Contains FASTA file with all the sequnces used in the anlaysis. Contains a META file associated with the FASTA 
file. The META contains Accession, Pangolin, Length, Country, Collection Date, Release Date, Genbank Title information for sequences in 
the FASTA file. 

2_processed_seqs : Second folder. Using Script 1 (varient_timeframes.script) the sequences from the FASTA file (in 1_raw_seqs) are 
seperated by time-interval/variant. 

3_aligned_seqs : Third folder. The reorganized sequnces (that are seperated by time-interval/lineage using Script 1) are aligned using 
MAFFt. 

4_consensus_seqs : Fifth folder:  The consensus sequnces for each aligned file from 3-aligned_seqs is constructed at different threshold 
(0.05, 0.1, 0.25, 0.75)
