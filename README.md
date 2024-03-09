As the data is imbalanced and with missing values,

3 imputation methods (zero impute, mean impute, and median impute) along with 4 sampling methods (stratified, random sampling, and random undersampling) are employed in the dataset. Hence, creating 12 different combinations of datasets (eg. zero imputed & stratified dataset) to perform an initial hyperparameter tuning (GridSearch) on the contamination value (most significant parameter in the IF model)

At the end of this stage, the  best combination of the imputation method and sampling method dataset along with the best contamination value is selected by evaluating the AUC score.

