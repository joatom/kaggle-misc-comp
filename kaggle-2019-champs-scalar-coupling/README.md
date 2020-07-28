# kaggle-2019-champs-scalar-coupling
This repository contains some of my codings and notes of the 2019 kaggle *Predicting Molecular Properties* competition (https://www.kaggle.com/c/champs-scalar-coupling) which ran from Jun/19 to Aug/19. The data was provided by the competition host CHAMPS (CHemistry And Mathematics in Phase Space).

The challange was to predict scalar couplings, a measure to indicate magnetic interaction of atoms in a molecoules. The data given mainly consisted of xyz coordinates of atoms in different molecules and some chemical/physical measures for the train data. I focused on the xyz values. I didn't had experiance with geometric problems and taggled the problem with common tabular approaches (ensemlbing XGBoost, LGBM, CatBoost and Tabular Neural Net). My solution ended up on place 916 of 2749. The better placed teams used GraphNeuralNets, PointNets or Transformers which are/were out of my skillset, yet ;-).


## Overview of notebooks
### /general
- **Nearest molecular neighbors**: a public kaggle kernel where I applied nearest neighbers in a pandas grouping function. It s rather slow, but shows how it's possible to apply complext grouping processings in pandas.

### /notes
(The notbooks are unpolished and uncommented.)
- **Pipeline**: description of the solution pipeline
- **Structures**: Basic geometric features, such as distance to k nearest neighbors (kNN)
- **Main-Features**: Cross Join Atoms per molecule to arange atoms pairwise. Pairwise features such as distances to common kNN. Angles between atoms.
- **nn-Model**: Tabular Neural Net
- **nn-Model-SKF**: Tabular Neural Net with StratifiedKFolding
- **xgb-Model**: XGBoost Model
- **lgb-Model**: LightGBM
- **cat-Model**: Cat Boost Model
- **blend-my-Models**: ensembling of single models and final submission
