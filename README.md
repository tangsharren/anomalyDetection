# Step 1: Handle imbalance & missing value
- As the data is imbalanced and with missing values, 3 imputation methods (*zero impute, mean impute, and median impute*) along with 4 sampling methods (*stratified, random sampling, and random undersampling*) are employed in the dataset. Hence, creating 12 different combinations of datasets (eg. zero imputed & stratified dataset) to perform an initial hyperparameter tuning (GridSearch) on the contamination value (most significant parameter in the IF model)
- At the end of this stage, the best combination of the imputation method and sampling method dataset along with the best contamination value is identified by evaluating the AUC score of IF model. The best combination of the imputation method and sampling method dataset is identified so that it can used for training other models too.

# Step 2: Tune all
- After that, the rest of the hyperparameters in IF model are further tuned to get the best model. 

# Step 3:Threshold
- The IF output is the anomaly score, a decision threshold is required to convert anomaly scores to binary labels. Therefore, we have to tune the threshold also. 
- Best-trained Isolation Forest model is used to generate anomaly scores for the test set.
- Then,using the anomaly scores generated optimizes the decision threshold by iterating over a range of thresholds and selecting the one that maximizes the ROC AUC score

# Step 4: Final model
- Final model is trained with the best hyperparameters and best threshold using the best combination of the imputation method and sampling method dataset.

Steps 2 to step 4 are repeated on the LOF model to identify the best LOF model


