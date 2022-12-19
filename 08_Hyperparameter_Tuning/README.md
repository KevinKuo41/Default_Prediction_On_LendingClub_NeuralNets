# Hyperparameter Tuning
#### We use grid search and apply 5-fold cross validation on the training dataset for hyperparameter tuning. 

## 1. Optimal Hyperparameters for NN2 Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through

| 10 Hyper Parameters  | Values | Range               |
|----------------------|--------|---------------------|
| Activation Function  | Tanh   | Tanh, ReLu, Sigmoid |
| Input Layer          | 42     | 42                  |
| Dropout Rate         | 0      | 0-0.5               |
| Hidden Layer 1       | 10     | 3-50                |
| Dropout Rate         | 0.2    | 0-0.5               |
| Hidden Layer 2       | 11     | 3-50                |
| Dropout Rate         | 0      | 0-0.5               |
| L2 Regularisation    | 0.001  | 0.1, 0.01, 0.001    |
| Learning Rate        | 0.001  | 0.001, 0.0001       |
| Epochs               | 100    | 1-100               |
