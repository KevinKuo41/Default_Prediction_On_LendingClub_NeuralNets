# Data Preprocessing
## 1. Checking Nans
#### (1) The feature variables related to "joint" have more than 80% of samples being Nans. <br><br> (2) For feature "emp_title", there are 20,000+ kinds of job titles in it. <br><br> (3) For feature "emp_length", around 10% of its samples are Nans. <br><br> (4) For feature "percent_bc_gt_75", around 2% of its samples are Nans.

## 2. Checking Data Structure
#### (1) Certain feature variables like "total_pyment" possess really high, maybe too high predicting power of defaulter. After conducting research on LendingClub's website, we know that these feature variables are recorded after issuing the loan. <br><br> (2) Some classes in some categorical features have very few instances so we consider merge some class to enhance its efficacy. <br><br> (3) For most continuous features, there are significant outliers, so we decide to exclude the outliers to better train the model.
