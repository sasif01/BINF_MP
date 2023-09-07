![image](https://github.com/sasif01/BINF_MP/assets/114173014/7448822c-5616-4bc8-8d6e-1bc0a13f118e)#Scoring Stability of Referance Genome

**Consensus Sequence (R)**

Generating a consensus allows ensures we can identify conserved sequences across all variants. Fallowing alignment, the consensus sequence for each alignment FASTA file is generated using the function consensusString in R. The threshold parameter is adjusted in order to compare the results when the minimum probability threshold for an agreement is different. When an agreement is not met, an 'N' is used in its place to specify the unknown nature of the base.

The fallowing is 

`# Get file path for each file
file_path <-dir_ls(path='./Data/aligned_seqs/4mn_2olp/')

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
}`
