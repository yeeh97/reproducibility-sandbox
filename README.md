# README
Acute Myeloid Leukemia Heatmap
==============================

Overview
--------

This project involves creating a heatmap for an Acute Myeloid Leukemia (AML) sample dataset sourced from [Shih et al., 2017](https://pubmed.ncbi.nlm.nih.gov/28193779/), pre-processed by [refinebio](https://www.refine.bio/). The dataset contains RNA-sequencing results for different types of AML under controlled treatment conditions. The goal is to visualize the gene expression patterns in the AML samples using a clustering heatmap.

Prerequisites
-------------

1.  RStudio: You can download it from [here](https://rstudio.com/products/rstudio/download/).
2.  R packages: `pheatmap`, `magrittr`, `readr`, `tibble`, `dplyr`.

You can install any missing packages using the command `install.packages("package-name")`.

Project Structure
-----------------

The project has the following structure:

-   `data`: This directory contains the dataset files.
-   `plots`: This directory will contain the generated plots.
-   `results`: This directory will contain the output of the analysis.

Usage
-----

1.  Clone this repository to your local machine.
2.  Open the R script in RStudio.
3.  Run the script. The script will automatically create the necessary directories, download and process the data, and generate the heatmap.

Code
----

The R script includes the following steps:

-   Setup: The script begins by checking if the necessary directories exist and creating them if they don't.

-   Data Import and Setup: The script reads in the metadata and data TSV files and assigns them to the variables `metadata` and `expression_df`, respectively.

-   Gene Selection: The script calculates the variance for each gene and filters the data to include only the genes in the upper quartile of variance.

-   Metadata Preparation: The script prepares the metadata for annotation by adding a new variable called `mutation`, which is based on the information from the accompanying paper.

-   Heatmap Creation: The script uses the `pheatmap()` function to generate a clustering heatmap.

Output
------

The script generates a heatmap, which visualizes the gene expression patterns in the AML samples. It also writes the selected genes to a TSV file in the `results` directory.

Resources
---------

For more information about R Markdown and creating dynamic analysis documents, visit the [R Markdown website](https://rmarkdown.rstudio.com/). The [RStudio community](https://community.rstudio.com/) is also a helpful resource for any questions about R Markdown and the R Markdown family of packages.

Contributions
-------------

Contributions to this project are welcome. Please note that this project is released with a Contributor Code of Conduct. By contributing to this project, you agree to abide by its terms.