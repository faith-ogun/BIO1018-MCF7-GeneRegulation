# Jupyter Notebooks for BIO1018 - MCF7 Gene Regulation Project

This folder contains the main Jupyter notebooks used throughout my **BIO1018 Final Year Dissertation** project. The notebooks cover everything from data preprocessing to training and fine-tuning models for predicting chromatin accessibility and gene expression in the MCF7 breast cancer cell line.

## 📂 Notebooks Overview
1. **`Data_Processing_Tutorial.ipynb`**  
   - This is the original tutorial from the GET paper, which served as the starting point for understanding how to process the data and apply the model.

2. **`prepare_mcf7_ATAC_only_ALL.ipynb`**  
   - Preprocesses ATAC-seq data for all chromosomes without separating them. Ideal for generating a complete dataset for downstream analysis.

3. **`prepare_mcf7_ATAC_only.ipynb`**  
   - Similar to `prepare_mcf7_ATAC_only_ALL`, but it separates the data by chromosome for easier analysis and validation.

4. **`finetune_mcf7_lo.ipynb`**  
   - Focuses on fine-tuning the GET model using preprocessed MCF7 data. This is crucial for improving the model's performance and adapting it specifically to MCF7 cells.

5. **`prepare_mcf7_git.ipynb`**  
   - My main preprocessing notebook with the most success. This is the core notebook for generating clean, ready-to-use data for the model.

6. **`pretrain_mcf7.ipynb`**  
   - Used for testing the model and pretraining data before moving on to fine-tuning.

## ⚡ Usage
- Open these notebooks with **Jupyter Notebook** or **JupyterLab**.
- Ensure you have installed all necessary dependencies.  
