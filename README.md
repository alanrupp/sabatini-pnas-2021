# Sabatini et al. 2021

This is the data and analysis scripts for the TRAP-seq data in Sabatini et al. *Proc Natl Acad Sci* 2021. This repo only contains the count files, analysis scripts, and figure panels. To generate the counts from the raw data, use the `shell` scripts in the each subfolder in data folder (Run*) with the FASTQ files from GEO ([GSE160257](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE160257)).

## Files
* **data**
  * **Run_1905**: count data and metadata from run Run_1905, plus information on mapping protocol
  * **Run_2487**: count data and metadata from run Run_2487, plus information on mapping protocol
  * `genes.csv`: file to map Ensembl gene_id to gene_name

* **figures**: output panels and assembled figures
  * **panels**: panel images
  * `figure.pdf`: compiled figure in PDF format
  * `figure.svg`: compiled figure in Inkscape SVG format

* **tools**
  * **rnaseq**: basic `R` functions and data for common analysis tasks with RNA-seq data

* `analysis.Rmd`: analysis script for count data
* `analysis.pdf`: knitted `rmarkdown` file of analysis
* `analysis.Rdata`: `R` image of workspace in `analysis.Rmd`

## Software
This analysis was run with:
* `R` 3.6.3
  * `tidyverse` 1.2.1
  * `knitr` 1.30
  * `kableExtra` 1.2.1
  * `ggrepel` 0.8.2
  * `pheatmap` 1.0.12
  * `Rtsne` 0.15
  * `DESeq2` 1.26.0
  * `wesanderson` 0.3.6
  * `reticulate` 1.16
  * `ggdendro` 0.1.21

## Output
In the command line, from the top folder run `R -e "rmarkdown::render('analysis.Rmd')"` to produce the output and figures.

## Citation
Sabatini PV,
