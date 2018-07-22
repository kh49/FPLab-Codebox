install miniconda
create new environment and install R
install bioconductor

install monocle - may need to revert R version during installs
install biobase
install devtools


install irlba -
library(devtools) (possible Rtools)

For R3.5.1:
assignInNamespace("version_info", c(devtools:::version_info, list("3.5" = list(version_min = "3.3.0", version_max = "99.99.99", path = "bin"))), "devtools")
install_github("bwlewis/irlba")
