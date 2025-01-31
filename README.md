# Python-Code
# Project Summary 
The use of data analytics and machine learning in risk management has become increasingly important for financial institutions to preempt and mitigate potential threats. This project aims to develop a data-driven solution for determining credit issuance for 1,000 pilot customers by leveraging a predictive model trained on a dataset of 24,000 existing clients. A Minimum Viable Product (MVP) model was built to classify customers as creditworthy (1) or not (0), optimizing the decision-making process to maximize profitability.
 

# Model Description
Constructed multiple classification models using existing credit card customer data to predict the likelihood of default. Each model was evaluated comprehensively using two key metrics: Accuracy Metrics, including the confusion matrix and its measures, AUC, ROC, and Gini coefficient, and Expected Profit Potential, calculated based on predicted outcomes from our model versus actual default data. To maximize expected profit, a threshold optimization algorithm was applied to determine the threshold that yielded the highest expected profit for each model. All models were assessed against these metrics, with the best-performing model primarily selected based on its ability to generate the highest expected profit, while accuracy metrics served as a secondary consideration.
 
# Data Pre-Processing and Exploratory Data Analysis (EDA)
The data was loaded and pre-processed to assess data types, handle missing values, and detect outliers. Key findings included:
•	Categorical Variables: Sex, Education, Repayment Status
•	Continuous Variables: Limit Balance, Age, Payment, and Bill Amounts
•	Data Completeness: All 24,000 entries contained valid values, with a "0" category used for missing data in the Education variable.
•	Outlier Detection:
o	99th percentile: Bill amounts ranged from 300K–350K, and payments from 65K–75K, with extreme values exceeding these thresholds.
o	1st percentile: Bill amounts ranged from -100 to -100, while payment values had a minimum of 0, indicating no issues.
•	Outlier Handling: Extreme values were retained as they were crucial for predictive modeling and accurately reflected pilot customer trends.
•Continuous Variables were binned and subsequently analyzed against default percentage for each bin.

<img width="476" alt="image" src="https://github.com/user-attachments/assets/c25e6465-5631-47a5-85ec-788df17156d3" />
<img width="480" alt="image" src="https://github.com/user-attachments/assets/c6571d89-453b-4d45-b6be-3531ac645d1b" />


<img width="485" alt="image" src="https://github.com/user-attachments/assets/17137c26-a570-42f1-aee9-25b28de7b8af" />
<img width="485" alt="image" src="https://github.com/user-attachments/assets/6f6f09de-eec4-482c-b39c-c5e91b985b9c" />


<img width="475" alt="image" src="https://github.com/user-attachments/assets/99f685a7-4b53-4542-967d-88e1507b181c" />
<img width="475" alt="image" src="https://github.com/user-attachments/assets/f94a12f5-3400-40c6-9784-3cc054a0f24b" />




From the analysis the following was observed:

•	Males have a higher default rate than females.
•	High school graduates show the highest default rates, while postgraduates have the lowest.
•	The "Other" marital status category has the highest default rate, followed by married and single.
•	Customers aged 70 and above have the highest default rate, with no clear pattern for other age groups.
•	Customers with payment delays have higher default rates, while those with zero balance, paid in full, or revolving credit tend to have lower rates.
•	Customers with lower limit balances show higher default rates, and this trend decreases as limit balance increases.
•	There is an inverse relationship between default rates and payment amounts; higher payments correlate with lower default rates.
•	A direct correlation is observed between higher bill amounts and increased default rates.
 

# Model Implementation

To ensure the model effectiveness, data was split into training and testing data. The training set is used to train the model, while the test set is used to validate the model's performance on unseen data. After appropriately segmenting the data and conducting hyperparameter tuning and threshold optimization to maximize profitability potential, the following modeling techniques were employed:
•	Logistic Regression
•	Logistic Regression with Recursive Feature Elimination (RFE)
•	Classification and Regression Trees (CART)
•	Random Forest
•	Gradient Boosting Machine (GBM)
•	Support Vector Machines (SVM)
•	Artificial Neural Networks with TensorFlow

To identify the optimal model, new features were generated from the existing data, and the models were rerun. Logistic Regression and Gradient Boosting Machine (GBM) emerged as the top performers, achieving AUC scores of 0.7896 and 0.7942, respectively, with expected profits of $984,500 and $948,500 on the test dataset. Although Logistic Regression had a slightly higher expected profit, GBM was chosen for its superior ability to capture complex feature interactions and handle non-linear relationships, allowing it to generalize more effectively to new, unseen data.

<img width="677" alt="image" src="https://github.com/user-attachments/assets/eec4142d-e809-4b9a-9f30-795a415bf0c1" />

Results from the Best Model: Gradient Boosting Machine
The Gradient Boosting Machine, along with the optimal threshold for profit maximization, was used to predict customer default risk, where "1" represented likely defaulters and "0" represented non-defaulters. Credit issuance decisions were based on the inverse likelihood of default—customers predicted to default ("1") were assigned a "0" for credit approval, and vice versa.

 

 



![image](https://github.com/user-attachments/assets/3481771b-b9b6-40fc-b4cf-111cf479b000)














