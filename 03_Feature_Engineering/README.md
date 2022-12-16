# Feature Engineering

## (1) Imputation:
#### - Due to 80%+ being NA, we converted “joint” tagged features into a categorical feature “co-borrower”. <br><br> - For “emp_length”, we replaced its NAs with “unknown”, as one of the categories.

####   -> 1 new feature is created

## (2) Feature Mutation:
#### - For features with most samples concentrated in a certain class and only few in others, we decided to merge minorities into one category, to make them more statistically meaningful (such as “pub_rec_bankruptcies”) <br><br> - We created “time_until_fc” (Credit Record Period) with counting the difference between “earliest_cr_line” and “issue_d”. <br><br> - We created “active_ratio_bc” (Ratio of Active Bankcard Account) by dividing “num_actv_bc_tl” by “num_bc_tl”. <br><br> - We created categorical feature “grade” with extracting the 1st letter from “sub_grade”. <br><br> - We created “open_rev_ratio” (Open Revolving Account Ratio) by by dividing “num_op_rev_tl” by “num_rev_accts”. <br>

####    -> 4 new features are created


## (3) Handling Outliers: 
#### Since we aim to find a general pattern for default prediction, we got rid of the samples with values located outside the Mean ± 3 times Standard Deviation.<br>

## (4) Deletion:
#### - For features updated after borrowers being default (“total_pymnt”, “total_rec_int”, “total_rec_late_fee”, “total_rec_prncp”), we exclude them from models, since they were unknown at the time when issuing the loan. (They are highly correlated to Default.) <br><br> - For features unrelated to the analysis (“zip_code” and “loan_id”), we deleted them all. <br><br> - For feature “emp_title”, there are 20,000+ kinds of job titles in it. Regardless of what kinds of adjustment we applied to it, we still cannot decrease its number of categories into a relatively reasonable range, so we exclude it from the models.<br>

## (5) Categorical Features Encoding:
#### - For categorical features, we conduct label encoding to convert categories into numbers since we will not implement linear models.<br>

## (6) Data Scaling:
#### - For Neural Network Models, standardising the features with a Mean of 0 and a Standard Deviation of 1 will significantly improve the models’ learning process.<br>

## After the entire process, we have **42** distinctive features in total. 
