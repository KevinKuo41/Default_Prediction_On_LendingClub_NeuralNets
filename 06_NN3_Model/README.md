# Setup of NN3 (NeuralNet With 3 Hidden Layers) Classification Model
#### 1. We apply Undersampling Approach as the rebalancing technique on the dataset for NN3 Model <br><br><br> 2. After 5-fold cross-validation for Hyperparameter tuning, the 12 optimal hyperparameters for NN3 Model: <br> (The details of Hyperparameter Tuning are outlined in 08_Hyperparameter_Tuning)

| 12 Hyper Parameters  | Values |
|----------------------|--------|
| Activation Function  | tanh   |
| Input Layer          | 42     |
| Dropout Rate         | 0      |
| Hidden Layer 1       | 10     |
| Dropout Rate         | 0.1    |
| Hidden Layer 2       | 22     |
| Dropout Rate         | 0.2    |
| Hidden Layer 3       | 41     |
| Dropout Rate         | 0.2    |
| L2 Regularisation    | 0.001  |
| Learning Rate        | 0.001  |
| Epochs               | 100    |     

#### 3. For the performance metrics, we use the Confusion Matrix, ROC Curve, False Negative Rate, Precision-Recall Curve, and Distribution of Predicted Default Probabilities (Please refer to the 09_Model_Comparison)
