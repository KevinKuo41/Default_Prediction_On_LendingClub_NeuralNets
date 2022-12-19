# Model Comparison

## 1. Confusion Matrix
### - NN2 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.82      | 0.62   | 0.71     | 104,291 |
| Default (1)    | 0.43      | 0.68   | 0.53     | 43,705  |
| Weighted Avg.  | 0.71      | 0.64   | 0.65     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208509015-0a9d333e-40c6-4102-bc5e-99886c5a9775.png)

### - NN3 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.81      | 0.67   | 0.73     | 104,291 |
| Default (1)    | 0.44      | 0.63   | 0.52     | 43,705  |
| Weighted Avg.  | 0.71      | 0.66   | 0.67     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208509034-ece63dee-73e2-4349-8e5b-d747dcbc9758.png)

### - NN4 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.82      | 0.62   | 0.71     | 104,291 |
| Default (1)    | 0.43      | 0.68   | 0.53     | 43,705  |
| Weighted Avg.  | 0.71      | 0.64   | 0.66     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208509043-43dabe50-7b86-4004-b797-450cac8e7e85.png)


## 2. ROC Curve
### - NN2, NN3 & NN4 Comparison

![圖片](https://user-images.githubusercontent.com/92542287/208509091-a7538788-0eed-47f3-a805-f255ffa17e3e.png)

## 3. Precision-Recall Curve
### - NN2, NN3 & NN4 Comparison

## 4. False Negative Rate
### - NN2, NN3 & NN4 Comparison
![圖片](https://user-images.githubusercontent.com/92542287/208509243-177491e5-ffcc-4ec8-bfdf-87b15787aeb3.png)


## 5. Distribution of Predicted Default Probabilities 
### - NN2 Model
![圖片](https://user-images.githubusercontent.com/92542287/208509377-a456107f-6cb8-4ef0-b523-a6a47fab472a.png)

### - NN3 Model
![圖片](https://user-images.githubusercontent.com/92542287/208509396-a88a40bc-5df1-435c-9ae7-0456e07fd4be.png)

### - NN4 Model
![圖片](https://user-images.githubusercontent.com/92542287/208509405-d0c7993a-2174-47a2-ac5f-c0884100b1e3.png)

## 6. Conclusion
#### The predicted default probabilities of the NN4 models almost concentrate on 20% to 80%. By contrast, the predicted default probability distribution of the NN2 & NN3 model is more evenly distributed (ranging from 10% to 80+%). Based on the comprehensive performance in the confusion matrix, AUC and FN Rate, we choose the NN2 model as the based model to make further lending decisions. 
