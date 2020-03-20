# - R - TUTORIAL
 - https://data-flair.training/blogs/rstudio-tutorial/
 

# R - Scripts R
- INSTALLED.PACKAGES - VERIFICA SE O PACOTE EXISTE


## COMANDO QUE VERIFICA SE O PACOTE EXISTE, CASO CONTRARIO INSTALA

pkgs <- c("RCurl","jsonlite")
for (pkg in pkgs) {
  if (! (pkg %in% rownames(installed.packages()))) { install.packages(pkg) }
}

## - COMANDO QUE INSTALA O H2O
install.packages("h2o", type="source", repos=(c("http://h2o-release.s3.amazonaws.com/h2o/latest_stable_R")))
