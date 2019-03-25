# How-to-tackle-Imbalance-Dataset

Dataset is availble on kaggle by Fraud Detection



Tips for performing under/over-sampling techniques with cross-validation

when cross-validating with oversampling, do the following to make sure your results are generalizable:

Inside the cross-validation loop, get a sample out and do not use it for anything related to features selection, oversampling or model building.

Oversample your minority class, without the sample you already excluded.

Use the excluded sample for validation, and the oversampled minority class + the majority class, to create the model.

Repeat n times, where n is your number of samples (if doing leave one participant out cross-validation).

If cross-validation is applied after over-sampling, basically what we are doing is overfitting our model to a specific artificial bootstrapping result. That is why cross-validation should always be done before over-sampling the data, just as how feature selection should be implemented. Only by resampling the data repeatedly, randomness can be introduced into the dataset to make sure that there won’t be an overfitting problem.
