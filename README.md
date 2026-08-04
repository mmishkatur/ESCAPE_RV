# ESCAPE_RV

A reverse vaccinology framework for protective antigen prediction in ESKAPE pathogens.

## Background
The ESKAPE group, *Enterococcus faecium*, *Staphylococcus aureus*, *Klebsiella pneumoniae*,
*Acinetobacter baumannii*, *Pseudomonas aeruginosa*, and *Enterobacter* species, accounts
for a large share of drug-resistant hospital infections. As antibiotic resistance spreads,
vaccines against these organisms have become an increasingly important line of defense, and
computational reverse vaccinology helps identify which proteins are worth pursuing as
protective antigens.

## The framework
ESCAPE_RV treats protective antigen discovery as a supervised prediction problem over
protein sequences. Protein language model (ESM-2) embeddings serve as the core predictive
signal, combined with ESMFold-based structural descriptors and physicochemical properties.
Candidates are evaluated with several model families, XGBoost, deep neural networks, a
fine-tuned ESM-2 classifier, and graph neural networks (GAT, TransformerConv, GPSConv) on
sequence-similarity graphs, with feature ablations and hyperparameter tuning throughout.

## The benchmark
`df_final_dataset_ready.csv`: a curated ESKAPE protective-antigen benchmark of 492 sequences,
228 positives (known protective antigens) and 264 negatives sampled from complete ESKAPE
proteomes.

## Contents
- `GNN_Antigen_Prediction_Structural_ESMFold_RUN_hpo.ipynb` — the full pipeline
- `df_final_dataset_ready.csv` — the benchmark
- `requirements.txt`, `LICENSE`

## Reproducing
Install `requirements.txt`, then run the notebook end to end in Jupyter. The ESM-2 and
ESMFold stages benefit from a CUDA GPU.

## A note on validation
This framework prioritizes candidates; it does not confirm them. Predicted protective
antigens require biological and experimental validation before use.

## Citation
If you use this repository, please cite the related thesis:

M Mishkatur Rahman. Machine Learning and Optimization Approaches for Protein Clustering,
Function and Vaccine Candidate Prediction. MS Thesis, North Dakota State University, 2026.

## License
MIT
