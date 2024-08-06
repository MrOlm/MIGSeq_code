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

# Installation guide

The python packages above can be installed using the following command:
```bash
pip install pandas==1.5.3 numpy==1.24.3 matplotlib==3.7.2 seaborn==0.11.2 scikit-learn==1.3.0 jupyter==1.0.0 notebook==6.5.4 ipykernel==6.22.0
```

To launch Jupyter Notebook, open a terminal (or Command Prompt on Windows) and navigate to the directory containing your notebook files. Then, launch Jupyter Notebook by running:
   ```bash
   jupyter notebook
```

Alternatively, Google Colab offers a free service where you can develop and run jupyter notebooks

Installation should complete in less than 5 minutes

# Demo

This demo provides a step-by-step guide to running the "MIGSeq_IgAProb_v1.ipynb" Jupyter Notebook, which processes and analyzes IgA binding probabilities using provided sample data. Follow these instructions to run the demo on your local environment.

## Instructions to Run the Demo

1. **Set Up Your Environment**:
   - Ensure that you have Python installed
   - Install necessary Python packages:
     ```bash
     pip install pandas numpy matplotlib seaborn scikit-learn jupyter
     ```
   - Clone or download the repository containing the "MIGSeq_IgAProb_v1.ipynb" notebook and the associated data files.

2. **Start Jupyter Notebook**:
   - Navigate to the directory containing the notebook file.
   - Start Jupyter Notebook by running:
     ```bash
     jupyter notebook
     ```

3. **Open the Notebook**:
   - In the Jupyter Notebook interface that opens in your web browser, navigate to and click on the "MIGSeq_IgAProb_v1.ipynb" file to open it.

4. **Edit data locations**:
   - Edit the variable "dataloc" to point to the folder where the file "SupplementalTable_S1_v1.csv" is located (this file is part of the supplemental files for the MIG-Seq publication)
   - Edit the variable "zenodoloc" to point to the folder where the file "IgASeq_genomeDetection_v4.csv" is located (this file is downloaded from the Senodo repo linked above)

5. **Run the Notebook**:
   - Execute the cells sequentially by clicking on each and pressing `Shift + Enter` or by using the "Run All" feature in the notebook's toolbar.

## Expected Output

- The notebook will output several pandas DataFrames showing the processed data, including calculated IgA binding probabilities and classifications into 'uncoated', 'low', and 'high' categories.

## Expected Run Time

- On a "normal" desktop computer, expect the entire notebook to run within approximately 1 minute
