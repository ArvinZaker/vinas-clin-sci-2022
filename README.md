# Reproducting analysis in the paper: Sex diversity in proximal tubule and endothelial gene expression in mice with ischemic acute kidney injury

This repository contains the report that reproduces some of the results from the study by Viñas et al. (2020).
A precomplied report is available as a `.html` file in the project's root directory (`report.html`).

## steps to reproduce the analysis

This analysis requires downloading the raw salmon files (`.sf`) from the study. 

To download the data for this analysis, follow these steps:

- go to the data entry for the paper [GSE144622](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE144622)
- go to the sample section and download the raw sf files from their respective entries. The files are from GSM4292460 to GSM4292483.
- The files download are in `.gz` format. Place them in the `./data/sf` folder
- Execute the following command to uncompress all files:


```
gunzip *.gz
```

- You can now recompile the report by using Rstudio `knitr` function or by executing the following command:


```
Rscript -e "rmarkdown::render('report.rmd', 'html_document')"
```


