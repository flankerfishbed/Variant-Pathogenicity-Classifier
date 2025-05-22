# Variant-Pathogenicity-Classifier
This project uses machine learning to predict whether a human genetic variant is likely pathogenic or benign, using annotated data from the ClinVar database. The model was trained on over 3.4 million variants, leveraging biologically meaningful features like variant type, allele length difference, and gene symbol structure.
# Variant Pathogenicity Classifier

Author: Ashwin R.  
Project: Predicting the clinical impact of human genetic variants using machine learning

This repository contains a machine learning pipeline that classifies human genetic variants as either pathogenic or benign, using annotated data from the ClinVar database.

Dataset

- Source: ClinVar `variant_summary.txt`
- Organism: Homo sapiens
- Format: Tab-separated, includes variant type, gene symbol, alleles, and clinical interpretation

 Features

- `gene_name_length`: length of the gene symbol
- `allele_length_diff`: ALT - REF allele length difference
- `variant_type_*`: one-hot encoded variant categories (e.g., deletion, duplication, SNV)

Model

- Random Forest Classifier (`scikit-learn`)
- Balanced class weights to account for label imbalance
- Evaluation via classification report and confusion matrix
- Feature importance visualized using both bar plots and SHAP values

Files

- `variant_pathogenicity_classifier_cleaned.ipynb`: full notebook (load data → model training → explainability)
- `rf_clinvar_model.pkl`: exported trained model
# Variant Pathogenicity Classifier


- `requirements.txt`: install dependencies to run locally

Install

```bash
pip install -r requirements.txt
