# AquaVax

AI-driven vaccine candidate prediction for bacterial pathogens of aquaculture.

## Overview
Bacterial disease is a persistent constraint on aquaculture, and deciding which of a
pathogen's proteins are worth pursuing as vaccine candidates is slow and labor-intensive
when done by experimental screening alone. AquaVax prioritizes vaccine candidate proteins
directly from sequence, combining protein language model embeddings, structure-informed
and physicochemical features, and graph-based learning. It targets four bacterial species
of particular importance to aquaculture: *Flavobacterium columnare*, *Flavobacterium
covae*, *Edwardsiella ictaluri*, and *Aeromonas hydrophila*.

## Dataset
`df_final_sequence.csv` — 526 labeled protein sequences: 92 reported vaccine candidates
(positives) and 434 non-candidates (negatives), curated from the literature.

## Methods
- Protein language model embeddings (ESM-2)
- Structure-informed features via ESMFold, plus physicochemical descriptors
- Protein similarity graphs for graph neural network models (GAT, TransformerConv, GPSConv)
- Comparison against XGBoost, deep neural networks, and a fine-tuned ESM-2 classifier
- Feature ablation and hyperparameter optimization

## Repository contents
- `Latest_GNN_Vaccine_Prediction_Structural_ESMFold_RUN_hpo.ipynb` — end-to-end notebook
- `df_final_sequence.csv` — curated dataset
- `requirements.txt`, `LICENSE`

## Requirements
See `requirements.txt`. Open the notebook in Jupyter; a CUDA-capable GPU is recommended for
the ESM-2 and ESMFold steps. Run the cells top to bottom.

## Notes
This is a computational prioritization tool; predicted candidates require experimental
validation. The work extends a study presented at the 2025 IISE Annual Conference and is
part of the author's MS thesis at North Dakota State University.

## Citation
Rahman, M. Mishkatur, Ayman Sajjad Akash, Harun Pirim, et al. "Machine Learning and Protein
Language Models for Vaccine Candidate Prediction in Aquaculture." IISE Annual Conference
Proceedings, 2025.
M. Mishkatur Rahman, MS Thesis, North Dakota State University, 2026.

## License
MIT
