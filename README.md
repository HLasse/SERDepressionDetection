# SERDepressionDetection

Code to reproduce the analysis from the paper "A Generalizable Speech Emotion Recognition Model Reveals Depression and Remission". This repository contains the models used for the analysis, i.e. the Bayesian mixture model, prognosis model, and BEST model. For the SER model, we refer to [Sechidis et al. (2021)](https://doi.org/10.1016/j.artmed.2021.102061).

## Structure
`Models.Rmd` contains all code for model creation.

`Plots.Rmd` contains all code for reproduction of figures and tables in both main manuscript and supplementary materials. Knitting the file/running the code will create the `figs` and `supplementary` folders where all plots will be saved.

`models/` contains the trained brms models. To re-train, delete or rename the files and run the code in `Models.Rmd`.

`data/` contains the output from the SER model for all time windows as well as non-sensitive participant metadata. 

`data/summary` contains CSV files of the aggregated MFCC features for the different window sizes. Window size is indicated by the file name. `None` means no windowing, i.e. aggregated over the entire recording. 
