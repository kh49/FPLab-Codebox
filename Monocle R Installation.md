#<b>Monocle Installation:</b>

install miniconda
create new environment and install R
install bioconductor
installdeseq2
install biobase

install monocle - may need to revert R version during installs

install devtools


install irlba -
library(devtools) (possible Rtools):
first: conda install r-git2r
in R:
install.packages("devtools")

For R3.5.1:
assignInNamespace("version_info", c(devtools:::version_info, list("3.5" = list(version_min = "3.3.0", version_max = "99.99.99", path = "bin"))), "devtools")

install_github("bwlewis/irlba")


download fasta files:

prefetch -t ascp -a "/export/home/khuang49/bin/miniconda3/pkgs/aspera-cli-3.7.7-0/bin/ascp|/export/home/khuang49/bin/miniconda3/pkgs/aspera-cli-3.7.7-0/etc/asperaweb_id_dsa.openssh" --option-file SRR_Acc_List.txt 
