# Feature Importance

## 1. NN2 Model
| Rank | Feature                           | Importance |
|------|-----------------------------------|------------|
| 1    | Sub-grade                         | 36.54%     |
| 2    | Term                              | 16.13%     |
| 3    | Grade                             | 16.11%     |
| 4    | Interest Rate                     | 11.75%     |
| 5    | Instalment                        | 3.76%      |
| 6    | Loan Amount                       | 3.75%      |
| 7    | Total High Credit Limit           | 3.14%      |
| 8    | Verification Status               | 2.74%      |
| 9    | Credit Inquiries In Past 6 Months | 2.46%      |
| 10   | Home Ownership                    | 2.36%      |

## 2. NN3 Model
| Rank | Feature                            | Importance |
|------|------------------------------------|------------|
| 1    | Sub-grade                          | 36.96%     |
| 2    | Interest Rate                      | 14.55%     |
| 3    | Grade                              | 14.30%     |
| 4    | Term                               | 11.63%     |
| 5    | Instalment                         | 4.59%      |
| 6    | Loan Amount                        | 4.08%      |
| 7    | Verification Status                | 3.44%      |
| 8    | Total Bankcard Credit limit        | 2.39%      |
| 9    | Monthly Debt Payments / Total Debt | 2.10%      |
| 10   | Credit Inquiries in Past 6M        | 1.86%      |

## 2. NN4 Model
| Rank | Feature                     | Importance |
|------|-----------------------------|------------|
| 1    | Sub-grade                   | 30.77%     |
| 2    | Grade                       | 16.06%     |
| 3    | Term                        | 15.22%     |
| 4    | Interest Rate               | 11.92%     |
| 5    | Verification Status         | 3.60%      |
| 6    | Loan Amount                 | 3.22%      |
| 7    | Home Ownership              | 2.97%      |
| 8    | Total High Credit Limit     | 2.74%      |
| 9    | Instalment                  | 2.22%      |
| 10   | Total Bankcard Credit limit | 2.06%      |

## 3. Comparison
#### We can find NN2, NN3 and NN4 models have almost the same selection of features, and the main difference between their feature importance is how they rank the features. Since they are all Neural Networks Model and use the exact mechanism, it is reasonable that they use almost the same features.

## 4. Underlying Mechanisms Between Features and Default
### (1) Grade & Sub-Grade
Grade is set based on the individual’s credit score, which takes account of the individual’s payment history and recent credit behaviour.
### (2) Interest Rate
Interest Rate on loans is decided based on the individual’s grade, so Grades and Interest Rate are highly related.
### (3) Repayment Term
Borrowers choosing 60 months as their repayment term have a bit higher probability of default, which may be related to the liquidity the borrower possesses.
### (4) Credit Inquiries in Last 6 Months
If a borrower has credit inquiry records in the last 6 months, it means that he/she had tried to borrow from other financial institutions and thus may have heavier financial burdens.
### (5) Home Ownership
Both are associated of borrower's financial stability
### (6) Verification Status
Document Verifications includes 1. Business Tax returns. 2. Proof of personal income. 3. Proof of identity and address for you or your business, so the candidate may have higher financial stability if candidate can provide these evidences
### (7) Instalment & Loan Amount & Interest Rate & Monthly Debt Payments / Total Debt
Interest Rate on loans is decided based on an individual’s grade, so they are highly related. A borrower with a higher interest rate and the loan amount will have a higher instalment, meaning they will need to pay more monthly. 
Instalment is the monthly payment owed by the borrower if the loan originates. Both Instalment & Monthly Debt Payments / Total Debt would impact the liquidity and saving ability of the borrower.
### (8) Total Bankcard Credit limit & Total High Credit Limit
Both are associated of borrower's liquidity
