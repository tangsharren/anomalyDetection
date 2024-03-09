As the data is imbalanced and exists missing values,

3 imputation methods (zero impute, mean impute, and median impute) along with 4 sampling methods (stratified, random sampling, and random undersampling)

are employed onto the dataset. Hence, creating 12 different combinations of dataset (eg. zero imputated & statified dataset) to perform an initial hyperparemeter tuning (GridSearch) on the contamination value (most significant parameter in IF model)

At the end of this stage, the  best combination of imputation method and sampling method dataset along with the best contamination value is selected by evaluating the AUC score.

