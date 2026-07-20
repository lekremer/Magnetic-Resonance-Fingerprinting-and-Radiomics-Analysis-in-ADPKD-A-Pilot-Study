# Magnetic Resonance Fingerprinting and Radiomics Analysis in ADPKD A Pilot Study
This study investigated radiomic features extracted from magnetic resonance fingerprinting (MRF)-acquired T1 and T2 quantitative maps in children and young adults with autosomal dominant polycystic kidney disease (ADPKD) with normal kidney function and compared these features to those extracted from MRF images of healthy volunteers.

The MATLAB folder contains:
1. Leave-one-patient-out LDA classifier with LASSO feature selection

## Description
MATLAB code implementing a leave-one-patient-out cross-validation
pipeline for binary classification using:
- LASSO generalized linear model feature selection
- Pearson correlation filtering
- Linear discriminant analysis classifier

## Requirements
MATLAB version R2025a
Statistics and Machine Learning Toolbox

## Input
Input feature file should be an excel or CSV table containing:
- ID: unique participant identifier
- Truth: binary outcome variable (0/1)
- Remaining columns: radiomic features

## Workflow
1. Load feature table
2. Perform leave-one-patient-out cross validation
3. Select features using LASSO within each training fold
4. Remove correlated features
5. Train LDA classifier
6. Generate classification performance metrics

## Outputs
- AUC
- Confusion matrix
- Classification scores
- Feature selection frequency
- Feature correlation heatmap
