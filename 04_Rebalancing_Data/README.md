# Rebalancing Data
#### In the dataset, 29.7% of the samples are defaulters and 70.3% of those are non-defaulters so we know this is a imbalanced dataset. To improve the performance of the Machine Learning Technique, we implement rebalancing approach to adjust the data. 3 rebalancing approaches - Oversampling, Undersampling, SMOTE are the most often used methods. <br><br> Since the 42 feature variables include some catergorical features, the SMOTE approach is not a suitable rebalancing tool for our dataset. (The main reason is that the implementation of SMOTE is based on the simulation with applying KNN. However, in catergorical features, the different figures only mean different classes instead of the real distance between samples.) <br><br> Thus, we test the implementation of the Oversampling and Undersampling approach on both Random Forest and XGBoost models, and choose the one with better Average Precision and F1-Score to conduct further model training. <br> (The scores below are the average scores of 5-fold split implementation on the training dataset of 75% samples)

## NN2 Model (Vanilla Neural Networks Model with 2 Hidden Layers)
#### Result: 
| Method        | F1-Score | Avg. Precision |
|---------------|----------|----------------|
| **Oversampling**  | **0.4259**   | **0.5222**         |
| Undersampling | 0.4190   | 0.5209         |
#### For NN2 Model, the Oversampling approach outperforms.

## NN3 Model (Vanilla Neural Networks Model with 3 Hidden Layers)
#### Result: 
| Method        | F1-Score | Avg. Precision |
|---------------|----------|----------------|
| Oversampling  | 0.5186   | 0.4386         |
| **Undersampling** | **0.5231**   | **0.4123**         |
#### For NN3 Model, the Undersampling approach outperforms.

## NN4 Model (Vanilla Neural Networks Model with 3 Hidden Layers)
#### Result: 
| Method        | F1-Score | Avg. Precision |
|---------------|----------|----------------|
| Oversampling  | 0.5063   | 0.4551         |
| **Undersampling** | **0.5170**   | **0.4330**         |
#### For NN4 Model, the Undersampling approach outperforms.
