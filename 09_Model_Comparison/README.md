# Model Comparison

## 1. Confusion Matrix
#### We can find that the Recall on Default of NN2 & NN4 moodels are much better than that of NN3 model, so we would prefer NN2 and NN4 to NN3.
### - NN2 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.82      | 0.62   | 0.71     | 104,291 |
| Default (1)    | 0.43      | 0.68   | 0.53     | 43,705  |
| Weighted Avg.  | 0.71      | 0.64   | 0.65     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208510032-a50a38f3-579e-4ae8-8cc0-ad6adc48fc29.png)

### - NN3 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.81      | 0.67   | 0.73     | 104,291 |
| Default (1)    | 0.44      | 0.63   | 0.52     | 43,705  |
| Weighted Avg.  | 0.71      | 0.66   | 0.67     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208510234-a5507320-d040-483d-81b5-969b676c01c5.png)

### - NN4 Model
| Class          | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Fully Paid (0) | 0.82      | 0.62   | 0.71     | 104,291 |
| Default (1)    | 0.43      | 0.68   | 0.53     | 43,705  |
| Weighted Avg.  | 0.71      | 0.64   | 0.66     | 147,996 |

![圖片](https://user-images.githubusercontent.com/92542287/208510460-4e1f0100-6334-4861-882f-fd1cc6602476.png)


## 2. ROC Curve
#### In terms of the ROC Curve, NN3's AUC is a bit higher than NN2's and NN4's, but the difference is so tiny that we can deem three as almostly the same.
### - NN2, NN3 & NN4 Comparison
| Model     | Area Under Curve |
|-----------|------------------|
| NN2 Model | 0.7077           |
| NN3 Model | 0.7081           |
| NN4 Model | 0.7072           |

![圖片](https://user-images.githubusercontent.com/92542287/208509703-9f28b5be-88d6-43c2-acfe-8dc499bed290.png)


## 3. Precision-Recall Curve
#### In terms of the Precision-Recall Curve, no matter how hard we tried to imporve the NN models, they still cannot achieve an over 50% average precision. Among them, the NN2 model achieve the highest AP of 49.03%. Frankly speaking, in the given dataset, the performance of NN models are worse than that of the XGBoost and RF models.
### - NN2, NN3 & NN4 Comparison
| Model     | Precision-Recall |
|-----------|------------------|
| NN2 Model | 0.4903           |
| NN3 Model | 0.4899           |
| NN4 Model | 0.4901           |

![圖片](https://user-images.githubusercontent.com/92542287/208509780-e8efb5f4-9f34-4f9b-a3a8-ac68a66aaf18.png)


## 4. False Negative Rate
#### False Negative Rate means that the probability that we falsely classify defaulters as non-defaulters. The lower, the better. We know that at the 50% Cut-off Level the NN2 and NN3 models outperform the NN4 model. The predicted default probabilities of the NN4 models almost concentrate on 20% to 80%. By contrast, the predicted default probability distribution of the NN2 & NN3 model is more evenly distributed (ranging from 10% to 80+%).
### - NN2, NN3 & NN4 Comparison
| Model     | False Negative Rate |
|-----------|---------------------|
| NN2 Model | 0.3191              |
| NN3 Model | 0.3653              |
| NN4 Model | 0.3233              |

![圖片](https://user-images.githubusercontent.com/92542287/208509874-b5b76aa4-fcb2-4920-9f50-35484beafaed.png)


## 5. Distribution of Predicted Default Probabilities
#### Unlike the XGBoost & RF Models, the output from Neural Networks Models is the default probability instead of a label so we don't need to apply calibration.
### - NN2 Model
![圖片](https://user-images.githubusercontent.com/92542287/208510123-1bd8ac7a-8815-45d4-a0d7-0db1a562a8d3.png)

### - NN3 Model
![圖片](https://user-images.githubusercontent.com/92542287/208510293-44754fc1-1055-4add-a002-bbcfd2ef0858.png)

### - NN4 Model
![圖片](https://user-images.githubusercontent.com/92542287/208510523-6056b944-1960-4f93-b860-1692a0c76ba2.png)


## 6. Conclusion
#### Based on the comprehensive performance in the confusion matrix, AUC and False Negative Rate, we choose the NN2 model as the based model to make further lending decisions. 
