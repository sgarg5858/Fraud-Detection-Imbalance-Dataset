# How-to-tackle-Imbalance-Dataset

Dataset is availble on kaggle by Fraud Detection



Tips for performing under/over-sampling techniques with cross-validation

when cross-validating with oversampling, do the following to make sure your results are generalizable:

Inside the cross-validation loop, get a sample out and do not use it for anything related to features selection, oversampling or model building.

Oversample your minority class, without the sample you already excluded.

Use the excluded sample for validation, and the oversampled minority class + the majority class, to create the model.

Repeat n times, where n is your number of samples (if doing leave one participant out cross-validation).
