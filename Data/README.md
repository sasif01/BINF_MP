1_raw_seqs : First folder. Contains FASTA file with all the sequnces used in the anlaysis. Contains a META file associated with the FASTA 
file. The META contains Accession, Pangolin, Length, Country, Collection Date, Release Date, Genbank Title information for sequences in 
the FASTA file. 

2_processed_seqs : Second folder. Using Script 1 (variant_timeframes.script) the sequences from the FASTA file (in 1_raw_seqs) are 
seperated by time-interval/variant. 

3_aligned_seqs : Third folder. The reorganized sequnces (that are seperated by time-interval/lineage using Script 1) are aligned using 
MAFFY. 

4_consensus_seqs : Fourth folder. The consensus sequnces for each aligned file from 3-aligned_seqs is constructed at different threshold 
(0.05, 0.1, 0.25, 0.75)

5_conserved_seqs : Fifth folder. The referance genome is scored and fragmented using Script 2 (variant_conservation.script) and the consensus sequnces in folders in 4_consensus_seqs/. The referance is fragememted into 100, 150 and 200 base pair fragments. 

6_features_files : Sixth folder. Scripts are used to get GC, AC, AG content. As well as determine other aspects.
