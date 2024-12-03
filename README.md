1 Data
The data set (see the csv file) contains information on default payments, demographic fac- tors, credit data, history of payment, and bill statements of credit card clients in Taiwan from April 2005 to September 2005. There are 25 variables:
• ID: ID of each client
• LIMIT BAL: Amount of given credit in NT dollars (includes individual and family/supplementary
credit)
• SEX: 1=male, 2=female
• EDUCATION: 1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown. Value 0 also appears in the data but not explained by the data provider.
• MARRIAGE: 1=married, 2=single, 3=others. Value 0 also appears in the data but not explained by the data provider.
• AGE: Age in years
1
• PAY 1: Repayment status in September, 2005. The meanings of various levels are: -1=pay duly, 1=payment delay for one month, 2=payment delay for two months, ... 8=payment delay for eight months, 9=payment delay for nine months and above. You also see -2 in the data, but its meaning is not explained by the data provider (could mean prepayment).
• PAY 2: Repayment status in August, 2005 (scale same as above)
• PAY 3: Repayment status in July, 2005 (scale same as above)
• PAY 4: Repayment status in June, 2005 (scale same as above)
• PAY 5: Repayment status in May, 2005 (scale same as above)
• PAY 6: Repayment status in April, 2005 (scale same as above)
• BILL AMT1: Amount of bill statement in September, 2005 (NT dollar)
• BILL AMT2: Amount of bill statement in August, 2005 (NT dollar)
• BILL AMT3: Amount of bill statement in July, 2005 (NT dollar)
• BILL AMT4: Amount of bill statement in June, 2005 (NT dollar)
• BILL AMT5: Amount of bill statement in May, 2005 (NT dollar)
• BILL AMT6: Amount of bill statement in April, 2005 (NT dollar)
• PAY AMT1: Amount of previous payment in September, 2005 (NT dollar)
• PAY AMT2: Amount of previous payment in August, 2005 (NT dollar)
• PAY AMT3: Amount of previous payment in July, 2005 (NT dollar)
• PAY AMT4: Amount of previous payment in June, 2005 (NT dollar)
• PAY AMT5: Amount of previous payment in May, 2005 (NT dollar)
• PAY AMT6: Amount of previous payment in April, 2005 (NT dollar)
• DEFAULT: Default status on payment in October of 2005 (1=yes, 0=no)


2 Problems
We are interested in predicting defaults in October of 2005. Consider the following models: logistic regression, random forest, support vector machine, and deep learning model based on a feed-forward neural network. You need to randomly split the data into the training set and the test set.
(1) Report accuracy, recall, precision, and AUC of these models on the test set and compare them. You can skip AUC for SVM because we didn’t discuss how to calculate it for this model.
(2) Which variables are important for predicting defaults?
Remark: You need to convert all categorical variables to one-hot vectors. You can use the OneHotEncoder class from sklearn.preprocessing or the PyTorch function torch.nn.functional.one hot().
2
