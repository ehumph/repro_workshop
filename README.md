# Acute Myeloid Leukemia Heatmap Analysis

This repository contains an analysis of an acute myeloid leukemia sample dataset, aiming to visualize the RNA-sequencing results for different types of AML under controlled treatment conditions. The original analysis was adapted from a [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html) and can be found in the repository's R Markdown file.

## Data

The analysis uses a dataset from [Shih et al., 2017](https://pubmed.ncbi.nlm.nih.gov/28193779/) that was pre-processed by [refinebio](https://www.refine.bio/). The dataset contains 19 samples from 19 acute myeloid leukemia (AML) model mice. You can download the dataset from [this page on refine.bio](https://www.refine.bio/experiments/SRP070849). The data is already [processed and quantile normalized](http://docs.refine.bio/en/latest/main_text.html#refine-bio-processed-refinebio-processedibadge).

## Set up

The analysis requires the creation of three folders: `data`, `plots`, and `results`. The `data` folder will contain the dataset, the `plots` folder will store the generated heatmap, and the `results` folder will include the results of the analysis.

## Libraries

The analysis uses the `pheatmap` library to create the heatmap. If the library is not already installed, the script will install it.

## Import and set up data

The data is imported as TSV files and stored as data frames in the R environment. The gene IDs are stored as row names.

## Choose genes of interest

After calculating the variance for each gene, the analysis selects genes in the upper quartile of variances.

## Prepare metadata for annotation

The analysis prepares the metadata for annotation by creating a variable to store the cancer type information.

