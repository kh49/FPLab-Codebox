# FPLab-Codebox
#coding notes:

##gencode transcript fasta processing for salmon:
Remove version numbers from gene and transcript IDs prior to indexing
"sed 's/\.[0-9][0-9]*//g' <transcriptsscrub.fa >scrubbed.fa"

gtfToGenePred
awk -v OFS='\t' '{print $1,$12,$2,$3,$4,$5,$6,$7,$8,$9,$10}'
