# ESCAPE_RV

A reverse vaccinology framework for protective antigen prediction in ESKAPE pathogens.

## Overview
The ESKAPE pathogens — *Enterococcus faecium*, *Staphylococcus aureus*, *Klebsiella
pneumoniae*, *Acinetobacter baumannii*, *Pseudomonas aeruginosa*, and *Enterobacter*
species — are leading drug-resistant bacteria behind many hospital-acquired infections,
and vaccines are an important complement to antibiotics against them. ESCAPE_RV is a
computational reverse vaccinology framework that prioritizes protective antigens directly
from protein sequence, using protein language model embeddings as the core predictive
layer alongside structure-informed and physicochemical features and graph neural networks.
The aim is to narrow large proteomes down to high-quality antigen candidates for
experimental follow-up.

## Dataset
`df_final_dataset_ready.csv` — a curated ESKAPE protective-antigen benchmark of 492
sequences: 228 positive (protective antigen) and 264 negative sequences, with negatives
drawn from complete ESKAPE proteomes.

## Methods
- Protein language model embeddings (ESM-2) as the core predictive layer
- Structure-informed features via ESMFold, plus physicochemical descriptors
- Sequence-similarity graphs for graph neural network models (GAT, TransformerConv, GPSConv)
- Comparison against XGBoost, deep neural networks, and a fine-tuned ESM-2 classifier
- Feature ablation and hyperparameter optimization

## Repository contents
- `GNN_Antigen_Prediction_Structural_ESMFold_RUN_hpo.ipynb` — end-to-end notebook
- `df_final_dataset_ready.csv` — curated ESKAPE benchmark
- `requirements.txt`, `LICENSE`

## Requirements
See `requirements.txt`. Open the notebook in Jupyter; a CUDA-capable GPU is recommended for
the ESM-2 and ESMFold steps. Run the cells top to bottom.

## Notes
Predicted antigen candidates require further biological and experimental validation; this
is a prioritization tool, not definitive identification. The framework is part of the
author's MS thesis at North Dakota State University (2026).

## Citation
M. Mishkatur Rahman, MS Thesis, North Dakota State University, 2026.

## License
MIT
