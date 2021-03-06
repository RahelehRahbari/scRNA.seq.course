---
output: html_document
---

# Technical requirements

## R-based

This course is based on the popular programming language [R](https://www.r-project.org/). However, one of the methods that we describe ([SNN-Cliq](http://bioinfo.uncc.edu/SNNCliq/)) is only partly R-based. It makes a simple _python_ call from R and requires a user to have write permissions to the working directory.

## Docker image

If you do not want to install all the packages required for the course manually, you can run a course docker image which contains all the required packages.

Make sure Docker is installed on your system. If not, please follow [these instructions](https://docs.docker.com/engine/installation/). To run the course docker image:

```
docker run -it quay.io/hemberg-group/scrna-seq-course:latest R
```

It will download the course docker image (may take some time) and start a new R session in a docker container with all packages installed and all data files available.

## Manual installation

If you are not using a docker image of the course, then to be able to run all code chunks of the course you need to clone or download the [course GitHub repository](https://github.com/hemberg-lab/scRNA.seq.course) and start an R session in the cloned folder. You will also need to install the following R packages:


```r
install.packages('devtools')
source('https://bioconductor.org/biocLite.R');biocLite('BiocInstaller')
devtools::install_github('hemberg-lab/scRNA.seq.funcs')

install.packages('pheatmap')
source('https://bioconductor.org/biocLite.R');biocLite('limma')

devtools::install_github('drisso/SingleCellExperiment')
devtools::install_github('grimbough/Rhdf5lib')
devtools::install_github('LTLA/beachmat')
devtools::install_github('davismcc/scater')
install.packages('statmod')
install.packages('mvoutlier')
devtools::install_github('MarioniLab/scran')
source('https://bioconductor.org/biocLite.R');biocLite('RUVSeq')

install.packages('penalized')
devtools::install_github('Vivianstats/scImpute')
devtools::install_github('theislab/kBET')
source('https://bioconductor.org/biocLite.R');biocLite('sva')

install.packages('irr')
devtools::install_github('hemberg-lab/SC3')
source('https://bioconductor.org/biocLite.R');biocLite('pcaMethods')
devtools::install_github('JustinaZ/pcaReduce')
install.packages('Seurat')
  
devtools::install_github('tallulandrews/M3Drop')

source('https://bioconductor.org/biocLite.R');biocLite('TSCAN')
source('https://bioconductor.org/biocLite.R');biocLite('monocle')
source('https://bioconductor.org/biocLite.R');biocLite('destiny')
devtools::install_github('jw156605/SLICER')

install.packages('ROCR')
source('https://bioconductor.org/biocLite.R');biocLite('DESeq2')
source('https://bioconductor.org/biocLite.R');biocLite('edgeR')
source('https://bioconductor.org/biocLite.R');biocLite('MAST')

source('https://bioconductor.org/biocLite.R');biocLite('MultiAssayExperiment')
source('https://bioconductor.org/biocLite.R');biocLite('SummarizedExperiment')
```
