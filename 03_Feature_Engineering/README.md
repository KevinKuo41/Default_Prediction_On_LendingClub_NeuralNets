# Feature Engineering

## (1) Imputation:
#### - Due to 80%+ being NA, we converted “joint” tagged features into a categorical feature “co-borrower”. <br><br> - For feature “emp_length”, we replaced its NAs with “unknown” as one of the categories.

####   -> 1 new feature is created

## (2) Feature Mutation:
#### - For features with most samples concentrated in a particular class and only a few in others, we decided to merge minorities into one category to make them more statistically meaningful (such as “pub_rec_bankruptcies”) <br><br> - We created “time_until_fc” (Credit Record Period) by counting the difference between “earliest_cr_line” and “issue_d”. <br><br> - We created “active_ratio_bc” (Ratio of Active Bankcard Account) by dividing “num_actv_bc_tl” by “num_bc_tl”. <br><br> - We created the categorical feature “grade” by extracting the 1st letter from “sub_grade”. <br><br> - We created “open_rev_ratio” (Open Revolving Account Ratio) by dividing “num_op_rev_tl” by “num_rev_accts”. <br>

####    -> 4 new features are created


## (3) Handling Outliers: 
#### Since we aim to find a general pattern for default prediction, we got rid of the samples with values located outside the Mean ± 3 times Standard Deviation.<br>

## (4) Deletion:
#### - For features updated after borrowers defaulted (“total_pymnt”, “total_rec_int”, “total_rec_late_fee”, “total_rec_prncp”), we excluded them from models since they were unknown at the moment when issuing the loan. (They are all highly correlated to default.) <br><br> - For features unrelated to the analysis (“zip_code” and “loan_id”), we deleted them all. <br><br> - Feature “emp_title” has more than 20,000 categories of job titles. No matter what kind of adjustment we applied to it, we still could not reduce its number of categories to be within a relatively reasonable range, so we excluded it from the models.<br>

## (5) Categorical Features Encoding:
#### - For categorical features, we conduct label encoding to convert categories into numbers since we will not implement linear models.<br>

## (6) Data Scaling:
#### - For Neural Network Models, standardising the features with a Mean of 0 and a Standard Deviation of 1 would significantly improve the models’ learning process. Thus, we did it for all feature variables. <br><br> - Standardisation was applied to all Numerical Features & Categorical Features. For Categorical Features, the standardisation would not affect what category a sample is sorted into but just the label value of categories in categorical features. The label value is just a tag with no numerical meaning, so it doesn't affect the result. <br>

## After the entire process, we have **42** distinctive features in total. 
