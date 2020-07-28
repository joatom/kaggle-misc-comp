# kaggle-2020-ARC
  
This repository contains some of my codings and notes of the 2020 kaggle *Abstraction and Reasoning Challenge (ARC)* competition (https://www.kaggle.com/c/abstraction-and-reasoning-challenge) which ran from March 2020 to May 2020.

The competition was set up with small logic ridles. The goal was to **exactly** predict one or two small images containing between 1 or 11 colors with size between 1x1 to 30x30 pixels. Only three to four training tasks per ridle where given. The train set containes 400 ridles, the evaluation set holds 100 samples and the hidden test set contained 100 riddles. Bronze medal could have been reached with accuratly predicting only 2%! of the test data.

## My Approaches
###  U-Net
My first approach was using an U-Net to generate the predictions. The challange here was tiny number of samples (only three to four per task!). Using pretrained models and applying augmentation I succesfully managed to predict 1% of the train data (unfortunately 0% on the test data).
### Rule based object detection I
All colors where separeted to one individual channel each. Neighboring pixels were marked as objects. Then rules color mapping rules were applied. On train set the algorithm scored 3% but 0% on the test set.
### Rule based object detection II
A better algorithm to detect objects was build. Rules with interacting objects were applied.

## Overview of notebooks
### /shared/u-net
- **[ARC] Exploring with UNet**: Public kaggle kernel with u-net

### /notes/object-detactor-I
- **[ARC] Simple Object Searcher**: Only submission to competition

### /notes/object-detactor-II
- **[ARC] Object Searcher 2**: 2nd Object detector and additional notes