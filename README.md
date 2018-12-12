# Telstra_Network_Challenge
Telstra is Australia's largest telecom provider. Based on a dataset on their service disruptions, I built a model predicting the severity of such disruptions, i.e. whether it's a minor glitch or a major outage. This project is based on a [Kaggle challenge](https://www.kaggle.com/c/telstra-recruiting-network) by Telstra.

[View the jupyter notebook here](https://nbviewer.jupyter.org/github/christopherbronner/Telstra_Network_Challenge/blob/master/Telstra_Network_Challenge.ipynb)

In the first part of the project, I consolidated the dataset, which was provided in several separate files. I then checked the data for missing values, outliers, and reformatted the features to be all numerical. In addition, I used one-hot encoding to convert non-ordinal categorical features to a series of binary features and grouped samples by event id.

I then built a simple classification model. The different classes were not balanced which is why I chose the F1 score as the appropriate metric. Using a random forest classifier, I achieved the best F1 score of 0.65. I used various feature selection techniques (selecting features based on correlation with the target, recursive feature elimination, PCA, and adding interaction features) in order to improve the model but the score did not improve significantly.
