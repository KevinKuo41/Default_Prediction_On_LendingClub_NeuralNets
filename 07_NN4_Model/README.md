# Setup of NN4 (NeuralNet With 4 Hidden Layers) Classification Model
#### 1. We apply Undersampling Approach as the rebalancing technique on the dataset for NN4 Model <br><br><br> 2. After 5-fold cross-validation for Hyperparameter tuning, the 13 optimal hyperparameters for NN4 Model: <br> (The details of Hyperparameter Tuning are outlined in 08_Hyperparameter_Tuning)

| 13 Hyper Parameters  | Values |
|----------------------|--------|
| Input Layer          | 42     |
| Dropout Rate         | 0      |
| Hidden Layer 1       | 22     |
| Dropout Rate         | 0.2    |
| Hidden Layer 2       | 7      |
| Dropout Rate         | 0.4    |
| Hidden Layer 3       | 48     |
| Dropout Rate         | 0.1    |
| Hidden Layer 4       | 50     |
| Dropout Rate         | 0.3    |
| L2 Regularisation    | 0.001  |
| Learning Rate        | 0.001  |
| Epochs               | 100    |    

#### 3. For the performance metrics, we use the Confusion Matrix, ROC Curve, False Negative Rate, Precision-Recall Curve, and Distribution of Predicted Default Probabilities <br> (Please refer to the 09_Model_Comparison)

