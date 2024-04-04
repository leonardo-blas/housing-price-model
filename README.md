# House price modelling challenge

## Problem statement
As part of a Kaggle competition, we were given house price datasets, `train.csv` and `test.csv`, from Ames, IA, between 2016 and 2020 [1]. We were asked to develop a model that can accurately predict the `SalePrice` column of the testing set, which was not given, and to optimize the RMSE, meaning to optimize our predictions in terms of dollars.

## Findings
* The best model is a 2nd degree ridge polynomial model. It's accuracy is  ~$ \pm $19k on the testing set ($r^2$ ~19k).
* The overall quality of a house has a high correlation with the sale price, but overall condition has a very low correlation.
* The year and month a house was sold have very low correlation with the sale price.
* The existence of a pool has a significant correlation with the sale price, but the pool area does not.

## Data dictionary
The data dictionary for the Ames housing dataset can be found at https://kaggle.com/competitions/adobe-dsb-34 [1].
Our model uses all ~80 columns except: `PID`, `Garage Yr Blt`, `MS SubClass`, `Overall Cond`, `BsmtFin SF 2`, `Low Qual Fin SF`, `Bsmt Half Bath`, `3Ssn Porch`, `Pool Area`, `Misc Val`, `Mo Sold`, `Yr Sold`.

## References
[1] J. O, M. Harris, "Ames Iowa Submission". 2024. https://kaggle.com/competitions/adobe-dsb-34.
