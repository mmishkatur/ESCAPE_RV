# ESCAPE_RV

Reverse vaccinology framework for protective antigen prediction in ESKAPE pathogens using protein language model embeddings, physicochemical and structural features, graph neural networks, and fine-tuned ESM-2.

## Overview

This repository contains the code and dataset used for computational protective antigen prediction in ESKAPE pathogens:

- *Enterococcus faecium*
- *Staphylococcus aureus*
- *Klebsiella pneumoniae*
- *Acinetobacter baumannii*
- *Pseudomonas aeruginosa*
- *Enterobacter* spp.

The framework evaluates multiple machine learning and deep learning approaches for antigen prioritization, including XGBoost, DNN, GAT, TransformerConv, GPSConv, and fine-tuned ESM-2.

## Repository Contents

- `df_final_dataset_ready.csv`  
  Final processed dataset used for model development and evaluation.

- `GNN_Antigen_prediction_Structural_ESMFold_...`  
  Notebook/script for feature-based and graph-based protective antigen prediction using ESM-2 embeddings, physicochemical descriptors, structural features, and graph neural networks.

## Methods

The workflow includes:

1. Dataset curation for ESKAPE protective antigen prediction
2. Feature extraction using:
   - ESM-2 protein language model embeddings
   - Physicochemical descriptors
   - Structural descriptors
3. Sequence-similarity graph construction
4. Model training and evaluation using:
   - XGBoost
   - Deep Neural Network (DNN)
   - Graph Attention Network (GAT)
   - TransformerConv
   - GPSConv
   - Fine-tuned ESM-2 sequence classifier
5. Ablation analysis across embedding-based, structural-feature, and combined feature settings

## Citation

If you use this repository, please cite the related thesis/manuscript:

M Mishkatur Rahman. *Machine Learning and Optimization Approaches for Protein Clustering, Function and Vaccine Candidate Prediction*. MS Thesis, North Dakota State University, 2026.

## Note

This repository is intended for research and computational vaccine candidate prioritization. Predicted antigen candidates require further biological and experimental validation.
