# Loan Selection Strategy (Threshold Selection)
#### Based on the comprehensive performance in the confusion matrix, AUC and False Negative Rate, we know that the NN2 model outperforms, so here we use the NN2 model to conduct further research on the Loan Selection Strategy and find the optimal predicted default rate threshold to achieve the highest profit when lending money on LendingClub platform.

## 1. Loans Screening Strategy Without Considering Cost of Capital
#### Like what we did in the "Default_Prediction_On_XGB_RF", we first took the average on loan returns of borrowers accepted under different default probabilities. Then, Our predicted default probabilities can serve as a threshold to decide which loans to accept. If we apply the predicted default probability of 31.2% as the threshold to screen the loans, we can reach the highest total profit. The green area below is the total profit we will get. (It's a bit different from the analysis in the "Default_Prediction_On_XGB_RF" since, in that project, our aim is to achieve the highest return on loans. However, here we aim to achieve the highest total profit.)

##### The optimal threshold of 31.2% (shown as the black spot) and its brought profit in green are shown in the below graph. 
![圖片](https://user-images.githubusercontent.com/92542287/208772860-23a45558-5010-4f6f-9782-f24f7ec1e022.png)

#### However, under real life condition, it is more reasonable to take account of the cost of capital. Thus, in the section 2, we will choose threshold based on the NPV.

## 2. Loans Screening Strategy With Considering Cost of Capital
#### (1) We noticed that the loans in the LendingClub dataset were issued from April 2016 to Sep 2020 in the USA, and the average cost of capital during this period was 1.8% (Based on Fred Economic data), so we use 1.8% as the discount rate to discount borrowers' cash flow into Present Value. <br>
#### (2) For borrowers, since we only have the data of their total payment instead of their payment per period, we need to make an assumption, which is we assume their outstanding debts occurred in the last several periods of their loan repayment. Based on the assumption, we can easily divide and sort their total payment into repayment amounts in each year within repayment term. <br><br> For example, supposing that one defaulter's loan amount is $15,000, his total payment is $10,000, and he is required to repay $5,000 per year, we would deem he successfully paid the first 2 years' instalments and defaulted the 3rd year's repayment. Based on our assumption, he repaid $5,000 in both the 1st and 2nd years and paid nothing in the 3rd year. <br>
#### (3) Once we have the repayment amount for each year and the discount rate, we can thus calculate the Net Present Value by:
$$Net\;Present\;Value = \sum_{i=1}^{5} \frac{Repayment_i}{(1 + Discount\;Rate)^i}\ - Loan\;Amount$$







