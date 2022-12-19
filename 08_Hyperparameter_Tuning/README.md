# Hyperparameter Tuning
#### We use grid search and apply 5-fold cross validation on the training dataset for hyperparameter tuning. 

Tuned hyperparameters include: 

1. The number of nodes in each layer
2. The dropout rate of each layer
3. The value of L2 penalties on kernel & bias
4. The learning rate
5. The number of epochs
6. The activation function can be either tanh, ReLu, or Sigmoid.
*For batch size, we use the default value of 32.


## 1. Optimal Hyperparameters for NN2 Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through

| 10 Hyper Parameters  | Values | Range               |
|----------------------|--------|---------------------|
| Activation Function  | tanh   | tanh, ReLu, Sigmoid |
| Input Layer          | 42     | 42                  |
| Dropout Rate         | 0      | 0-0.5               |
| Hidden Layer 1       | 10     | 3-50                |
| Dropout Rate         | 0.2    | 0-0.5               |
| Hidden Layer 2       | 11     | 3-50                |
| Dropout Rate         | 0      | 0-0.5               |
| L2 Regularisation    | 0.001  | 0.1, 0.01, 0.001    |
| Learning Rate        | 0.001  | 0.001, 0.0001       |
| Epochs               | 100    | 1-100               |

## 2. Optimal Hyperparameters for NN3 Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through

| 12 Hyper Parameters  | Values | Range               |
|----------------------|--------|---------------------|
| Activation Function  | tanh   | tanh, ReLu, Sigmoid |
| Input Layer          | 42     | 42                  |
| Dropout Rate         | 0      | 0-0.5               |
| Hidden Layer 1       | 10     | 3-50                |
| Dropout Rate         | 0.1    | 0-0.5               |
| Hidden Layer 2       | 22     | 3-50                |
| Dropout Rate         | 0.2    | 0-0.5               |
| Hidden Layer 3       | 41     | 3-50                |
| Dropout Rate         | 0.2    | 0-0.5               |
| L2 Regularisation    | 0.001  | 0.1, 0.01, 0.001    |
| Learning Rate        | 0.001  | 0.001, 0.0001       |
| Epochs               | 100    | 1-100               |

## 3. Optimal Hyperparameters for NN4 Model
#### The values in column Values are the optimal parameters, and the values in column Range are the range of numbers we grid search through

| 14 Hyper Parameters  | Values | Range               |
|----------------------|--------|---------------------|
| Activation Function  | tanh   | tanh, ReLu, Sigmoid |
| Input Layer          | 42     | 42                  |
| Dropout Rate         | 0      | 0-0.5               |
| Hidden Layer 1       | 22     | 3-50                |
| Dropout Rate         | 0.2    | 0-0.5               |
| Hidden Layer 2       | 7      | 3-50                |
| Dropout Rate         | 0.4    | 0-0.5               |
| Hidden Layer 3       | 48     | 3-50                |
| Dropout Rate         | 0.1    | 0-0.5               |
| Hidden Layer 4       | 50     | 3-50                |
| Dropout Rate         | 0.3    | 0-0.5               |
| L2 Regularisation    | 0.001  | 0.1, 0.01, 0.001    |
| Learning Rate        | 0.001  | 0.001, 0.0001       |
| Epochs               | 100    | 1-100               |
