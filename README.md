# MIGSeq_code

This repository holds code supporting the publication "Metagenomic Immunoglobulin Sequencing (MIG-Seq) Exposes Patterns of IgA Antibody Binding in the Healthy Human Gut Microbiome".

The notebooks use data from the supplemental information of this publication, as well as additional data hosted on Zenodo: [https://doi.org/10.5281/zenodo.10367211](https://doi.org/10.5281/zenodo.10367211)

# Description

The uploaded Jupyter Notebook titled "MIGSeq_IgAProb_v1.ipynb" contains a series of data processing and analysis steps related to the study of immunoglobulin A (IgA) binding probabilities in various samples. Here is an overview of its main functions:

### Data Loading and Preparation
The notebook starts by loading raw abundance data into a pandas DataFrame. This data includes the metrics "genome", "Tube_ID", "breadth", "relative abundance (rel_ab)", and "sample".

### Data Merging and Cleaning
The data is split into subsets based on different conditions (e.g., 'positive' and 'unsorted' IgA) and then merged on the common columns 'genome' and 'Tube_ID'. The merged DataFrame is cleaned to ensure there are no duplicates and to handle missing values. For instance, NaNs in certain columns are replaced with zeros based on specific conditions.

### Calculation and Classification
The notebook includes calculations to derive new metrics from the existing data. The code calculates a normalized IgA binding probability (IgA_prob) for each sample, and the function `calc_class` is defined and used to classify the IgA binding probabilities into different classes ('uncoated', 'low', 'high') based on thresholds.

In summary, the notebook processes and cleans IgA-related data, merges different subsets, computes derived metrics, and classifies the samples into distinct binding classes for further analysis and visualization.

# System requirements

## Operating System

- **Linux**: Ubuntu 20.04.6 LTS (Kernel version: 5.4.0-182-generic)
- Other operating systems should work as well, including macOS and Windows, as long as they can run jupytyer notebooks

## Python

- **Python**: 3.10.10
- Other Python versions (>=3.7) should work just fine as well

## Python Packages

The following Python packages are required. They are listed with their respective version numbers:

- pandas==1.5.3
- numpy==1.24.3
- matplotlib==3.7.2
- seaborn==0.11.2
- scikit-learn==1.3.0
- jupyter==1.0.0
- notebook==6.5.4
- ipykernel==6.22.0

These packages can be installed using the following command:
```bash
pip install pandas==1.5.3 numpy==1.24.3 matplotlib==3.7.2 seaborn==0.11.2 scikit-learn==1.3.0 jupyter==1.0.0 notebook==6.5.4 ipykernel==6.22.0
