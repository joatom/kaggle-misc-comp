# Solution pipeline
The models were devided according to the six different atom combinations (e.g. 1JHC, 1JHN, 3JHC,...) to predict.
## Feature Engineering
I developed those features (*see structures.ipynb*, *main-features.ipynb*), which are used in various combinations in the models:
- distance (cosine, euclidean)
- 10 nearest neighbors (incl. ranked by distance, coordinates)
- pca
- number of atoms per molecule
- pairwise features
  - common k nearest neighbors (kNN) of two atoms
  - distance of atom pairs and common kNN
  - angles between common kNN and atom pairs
  - dihedral angle
  - center of pairs

## Single Models
- Tabular neural net (NN) with random validation split (best performing single model)
- NN with StratifiedKFold
- XGBoost
- LGBM
- CatBoost

## Ensembling
The single models were blended with a seperate XGBoost-Model. I grouped result ranges of validation and single model prediction in bins to construct an additional feature. 
