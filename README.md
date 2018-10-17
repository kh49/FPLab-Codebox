# FPLab-Codebox
#coding notes:

##gencode transcript fasta processing for salmon:
Remove version numbers from gene and transcript IDs prior to indexing
`sed 's/\.[0-9][0-9]*//g' <transcriptsscrub.fa >scrubbed.fa

gtfToGenePred -genePredExt -geneNameAsName2 -ignoreGroupsWithoutExons gtf genepred 

awk -v OFS='\t' '{print $1,$12,$2,$3,$4,$5,$6,$7,$8,$9,$10}'`

#lab serve folder config:
`folders = \\PFServer\folder
username = PFServer\username`

# bacterial genome fasta processing
convert fasta to first have sequence in one line

`awk '/^>/ {printf("%s%s\n",(N>0?"\n":""),$0);N++;next;} {printf("%s",$0);} END {printf("\n");}' GCA_000018125.1_ASM1812v1_genomic.fna > Streppyogenes_NZ131.fa`

extract PCR region defined by Primer Blast with start and length

`awk '1==NR{print $0;next} 2==NR{print substr($0,17072,4226)}' Streppyogenes_NZ131.fa > Streppyogenes_NZ131_16S_23S_1.fa`
