**Stability Scores**

**Consensus Sequence (R)**

Generating a consensus allows ensures we can identify conserved sequences across all variants. Fallowing alignment, the consensus sequence for each alignment FASTA file is generated using the function consensusString in R. The threshold parameter is adjusted in order to compare the results when the minimum probability threshold for an agreement is different. When an agreement is not met, an 'N' is used in its place to specify the unknown nature of the base.

**4mn_ovlp**
The fallowing is used to generate files (5 in total, for each threshold) using the aligned sequences in 3_aligned_seqs/4mn_2ovlp/

```
# Get file path for each file
file_path <-dir_ls(path='./Data/3_aligned_seqs/4mn_2olp/')

# Adjust parameter (threshold) to alter level of conversations across sequences` 
for ( j in c(0.05, 0.1, 0.25, 0.5, 0.75)){
  file_content=c()
  for (i in seq_along(file_path)){
    file_content[i] <- consensusString(readDNAMultipleAlignment(file_path[[i]]), ambiguityMap='N', threshold=j)
  }
  # Setting name of each consensus`
  file_content <- set_names(file_content, paste0('>',word(file_path, 5L, sep = '/')))
  # Writing all consensus seqs for each time range to a single file `
  write(paste(names(file_content), file_content, sep = '\n'), paste0('Consensus_',j))
}
```


**46mn_olp**
The fallowing is used to generate files (5 in total, for each threshold) using the aligned sequences in 3_aligned_seqs/6mn_2olp/

```
# Get file path for each file
file_path <-dir_ls(path='./Data/3_aligned_seqs/6mn_2olp/')

# Adjust parameter (threshold) to alter level of conversations across sequences 
for ( j in c(0.05, 0.1, 0.25, 0.5, 0.75)){
  file_content=c()
  for (i in seq_along(file_path)){
    file_content[i] <- consensusString(readDNAMultipleAlignment(file_path[[i]]), ambiguityMap='N', threshold=j)
  }
  # Setting name of each consensus
  file_content <- set_names(file_content, paste0('>',word(file_path, 5L, sep = '/')))
  # Writing all consensus seqs for each time range to a single file 
  write(paste(names(file_content), file_content, sep = '\n'), paste0('Consensus_',j))
}
```
