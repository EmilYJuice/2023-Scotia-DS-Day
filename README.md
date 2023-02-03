# 2023-Scotia-DS-Day
:star:Winter 2023 Scotiabank Data Science Discovery Day (Credit Card Fraud Detection)

### Background
The widespread use of credit cards in Canada, coupled with the increase in online transactions during 
the Covid-19 pandemic, has made credit card fraud a significant problem. With over 801 million 
credit cards in circulation in 2021 and more than 6 billion2
purchase transactions made each year in 
Canada, fraudsters have been using credit cards to obtain goods and services without paying. This 
not only harms the profitability of financial institutions and the security of consumers, but it also 
poses a threat to the stability of the financial system as a whole. As the intensity of transaction fraud 
continues to increase, it is essential for financial institutions and consumers to take steps to prevent 
and mitigate the impact of this crime.

### About Data
• 89,230 records in the training dataset; 22,307 records in the test dataset

• Each record is a credit card transaction, 1 ID column (TRANSACTION_ID) to uniquely
identify a transaction

• 1 target column (FRAUD_FLAG): whether a transaction is labeled as fraud after fraud 
review 

• 173 features, description of features is available in data dictionary

### Methods
• Technical: Extra Data, Data imputation by mode, create new column with null/not null, Correlation, Min-max Scaler, Frequency Encoding, XGBoost (setting weighted by label), Fine-tuning to maximize AUC-ROC.

• Maximal F-1 Score: Decrease Prediction Thresholds

### Interpret The Result:
• Visualization (correlation heat Map and Bar charts)

• Fraud-detection Score (low, medium and high groups)

• Identify Fraud Groups - for important columns, split data into 10 groups and compare density of target labels

### Business Suggesstions:
The system reduces the cost of organization/groups, and detect fraud transactions better than human
Customer Experience (Explain the model by important attributes, Double Check results when in the medium group by Fraud Detection System)

Transactions to Decline (Fraud Scoring System, Decline Transaction in High Risk Groups, may have more detection on dangerous groups, such as

• Transaction Amounts in the range (169.12, 73126.95] account for 10% of data
but 25.3% of fraud flag

• 12:00 am to 8:45 am each day, fraud rate is more than twice

• Less credit limit leads to more fraud

• Number of phone orders/number of purchase for excluding gas < 3 times for the past 30 days takes up to 45.6% and 47.12% of fraud flag respectively

:sparkles:Long term suggesstions (Updating the model (model stacking, bagging, train different models with different groups)), NLP (example: on comments in transactions), Other AI models (Deep learning, Random Forest, Adaboost), Collaborating with other organizations to gain more data and discuss models

### :blush:Check our PPT, notebook, and brief write-up~
