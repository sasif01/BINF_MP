**Description**: Files in this directory are the results from Script 1 (varient_timeframes.script). The sequence data needed to be pre-processed before alignment and analysis. Specifically, sequences were grouped by Lineage (Omicron, Delta, Beta, etc.) and separated by PANGO lineage **variant** designations. Lineages with only a single variant (Alpha, Delta, etc.) were further separated into fixed time-intervals to track their evolution. This is done so the evolution of each lineage can be tracked over fixed time periods or through the emergence of newer variants.


**4mn_2olp** : 4-month time interval, 2 month overlap
**Script1 Settings**:
Running script (in BINF_MP folder) : python3 Code/variant_timeframes.script Data/1_raw_seq/lineages.meta Data/1_raw_seq/lineages_one.fasta
  User Input Settings : delimiter = ',' , time interval = 4, overlap = 2

**6mn_2ovl** :6-month time interval, 2 month overlap
**Script1 Settings**
Running script (in BINF_MP folder) : python3 Code/variant_timeframes.script Data/1_raw_seq/lineages.meta Data/1_raw_seq/lineages_one.fasta
  User Input Settings : delimiter = ',' , time interval = 6, overlap = 2


The fasta and metadata file is used to seperate out the sequences (using Script 1- variant_timeframes.script) based on specified time-interval and overlap or by varient 
