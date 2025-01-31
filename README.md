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
•	Continuous Variables were binned and subsequently analyzed agains

<img width="510" alt="image" src="https://github.com/user-attachments/assets/da23f96c-1531-43a3-8b1a-05027d2e8826" />
<img width="512" alt="image" src="https://github.com/user-attachments/assets/ef980061-df02-4ff7-a37f-ef831667c454" />



<img width="486" alt="image" src="https://github.com/user-attachments/assets/313478a6-4d0b-4fb3-abd2-3492ad8b4280" />
<img width="511" alt="image" src="https://github.com/user-attachments/assets/0a4e693b-185f-4e10-9d4a-582832c35102" />


