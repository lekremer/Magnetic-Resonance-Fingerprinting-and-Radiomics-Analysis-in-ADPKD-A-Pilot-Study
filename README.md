# A pilot study of magnetic resonance fingerprinting and radiomics analysis in autosomal dominant polycystic kidney disease

This repository contains example MATLAB code used in the study investigating radiomic features extracted from magnetic resonance fingerprinting (MRF)-acquired T1 and T2 quantitative maps in children and young adults with autosomal dominant polycystic kidney disease (ADPKD). Radiomic features from participants with ADPKD and preserved kidney function were compared with those extracted from healthy volunteers.

**Note:** Imaging data and participant data are not included because of institutional data-sharing restrictions.

## Repository Contents

### MATLAB
- Leave-one-patient-out linear discriminant analysis classifier with LASSO feature selection

## Description

This MATLAB script implements a leave-one-patient-out cross-validation pipeline for binary classification using:

- LASSO generalized linear model (GLM) feature selection
- Pearson correlation filtering
- Linear discriminant analysis (LDA) classifier

## Requirements

- MATLAB R2025a
- Statistics and Machine Learning Toolbox

## Input

The input feature table should be provided as an Excel (`.xlsx`) file containing:

- **ID** – Unique participant identifier
- **Truth** – Binary outcome variable (0/1)
- **Remaining columns** – Radiomic features

## Workflow

1. Load the feature table.
2. Perform leave-one-patient-out cross-validation.
3. Select features using LASSO within each training fold.
4. Remove highly correlated features using Pearson correlation filtering.
5. Train an LDA classifier.
6. Evaluate model performance.

## Outputs

- Area under the ROC curve (AUC)
- Confusion matrix
- Predicted classification scores
- Feature selection frequency
- Feature correlation heatmap
