# Loan Selection Strategy (Threshold Selection)
#### Based on the comprehensive performance in the confusion matrix, AUC and False Negative Rate, we know that the NN2 model outperforms, so here we use the NN2 model to conduct further research on the Loan Selection Strategy and find the optimal predicted default rate threshold to achieve the highest profit when lending money on LendingClub platform.

## 1. Loans Screening Strategy Without considering Cost of Capital
#### Like what we did in the "Default_Prediction_On_XGB_RF", we first took the average on loan returns of borrowers accepted under different default probabilities. Then, Our predicted default probabilities can serve as a threshold to decide which loans to accept. If we apply the predicted default probability of 31.2% as the threshold to screen the loans, we can reach the highest total profit. The green area below is the total profit we will get. (It's a bit different from the analysis in the "Default_Prediction_On_XGB_RF" since, in that project, our aim is to achieve the highest return on loans. However, here we aim to achieve the highest total profit.)

##### The optimal threshold of 31.2% (shown as the black spot) and its brought profit in green are shown in the below graph. 
![圖片](https://user-images.githubusercontent.com/92542287/208772860-23a45558-5010-4f6f-9782-f24f7ec1e022.png)

#### However, under real life condition, it is more reasonable to take account of the cost of capital.








