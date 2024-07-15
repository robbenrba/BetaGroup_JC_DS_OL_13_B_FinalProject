# finalProject
Final Project, JCDSOL-013(B), Roberto Benedict & Gretty Margaretha

### Context :
Bank marketing campaigns dataset analysis - Opening a Term Deposit dataset is a dataset describing a Portugal bank marketing campaigns results. Conducted campaigns were based mostly on direct phone calls, offering bank client to place a term deposit.

**Socio-economic conditions in the campaign period: May 2008 to June 2013**
- Post global financial crisis effects in Portugal
- Bank restructuring of Banco Montepio

Due to the nature of the conditions during the period, a potential client would also have lower interest in subscribing for term deposit, which in turn would make cost of outreach or promotion cost higher to accomodate the lower interest of the clients. 

If after all marketing efforts client had agreed to place deposit - target variable marked 'yes', otherwise 'no'

Target y (term): 

* 0 : no, disagree to place deposit
* 1 : yes, agree to place deposit

### Problem Statement :

The marketing process can consume significant time and resources if the bank targets all potential clients without prior filtering or targeted marketing, resulting in wasted time and resources. The effects are more dramatic in the post global financial crisis socio-economic conditions bringing about the crucial requirement of the bank to prioritize minimizing costs due to the higher reaching out cost for new clients in the economic climate. The bank wants to increase marketing efficiency by identifying which potential clients are likely to agree to open a term deposit account.

### Goals :
1. Identify client feature patterns for the most probable potential clients:
    * Most important features correlated with the target
    * Seasonality
    * Socio-economic conditions
2. Minimize revenue loss through promotion costs minimization : How much budget allocation percentage would be minimized ?

Based on these issues, the bank aims to predict the likelihood of a client agreeing to open a term deposit account. This can support the bank in executing marketing strategies focused on clients most likely to be interested, thereby saving costs, time, and resources.

Additionally, the bank wants to understand the factors influencing a client's decision to open a term deposit account or not, enabling them to develop better plans for approaching potential clients.

## Analytic Approach
Analisis data customer akan dilakukan untuk menemukan pola tertentu yang dapat membedakan customer yang berpotensi akan churn atau tidak. Tahap selanjutnya, model klasifikasi akan dibuat untuk membantu perusahaan agar dapat melakukan prediksi kemungkinan seorang customer akan melakukan churn atau tidak.

### Goals :
1. Identify client feature patterns for the most probable potential clients:
    * Most important features correlated with the target
    * Seasonality
    * Socio-economic conditions
2. Minimize revenue loss through promotion costs minimization : How much budget allocation percentage would be minimized ?

Based on these issues, the bank aims to predict the likelihood of a client agreeing to open a term deposit account. This can support the bank in executing marketing strategies focused on clients most likely to be interested, thereby saving costs, time, and resources.

Additionally, the bank wants to understand the factors influencing a client's decision to open a term deposit account or not, enabling them to develop better plans for approaching potential clients.

### Stakeholder :
* Bank marketing division : as main the stakeholder and the user of the resulting model, marketing division will minimize promotion cost by minimizing revenue loss through lower promotion cost due to more targeted marketing.

## Machine Learning Workflow
Below is the description of the program workflow in the IPYNB file.
1. Data Cleaning
2. Data Analysis
3. Data Preparation
4. Modeling and Evaluation
5. Drawing conclusions from the insights obtained.

## Kesimpulan
#### Data Analysis

In our data analysis, we focused exclusively on customer features to better understand their behavior and improve marketing strategies. The analysis explored various dimensions such as job types, marital status, education levels, credit defaults, housing and personal loans, contact communication methods, and timing of marketing efforts. We found that customers with different job types, marital statuses, and education levels show varying tendencies towards making deposits. For instance, single customers and those with professional education are more likely to make deposits. Interestingly, the presence of housing loans does not significantly influence deposit decisions, while personal loans are more common among customers. Effective marketing is facilitated through cellular contact and is most successful when conducted from Tuesday to Thursday. Seasonal trends also play a role, with March being a particularly effective month for securing deposits. Additionally, older customers, especially those in their 60s, are more likely to save in term deposits due to their stable financial situations. The analysis also highlighted the importance of the duration of contact and the positive influence of past campaign successes on current outcomes. However, it is crucial to note that certain high correlations among bank-related features, such as employment variation rate and consumer price index, are beyond the control of the marketing team.


#### Machine Learning

Based on the classification report results from the model, if the model is used to predict the list of customers who will deposit, it can reduce the promotional budget allocation by 93% for customers who are likely to be loyal or not deposit, allowing the company to focus costs or even eliminate them. Additionally, the model can identify 78% of depositing customers out of all potential depositing customers based on recall.

This model has a precision of 70% for predicting depositing customers. This means that each time the model predicts a customer will deposit, there is approximately a 70% chance that the prediction is correct. However, there is still a false positive rate, with about 7% of non-depositing customers being incorrectly predicted as depositing customers based on recall.

Assuming the promotional cost per customer is 50 USD and the total number of customers in a given period is 200, with 100 of them depositing, the business scenario can be calculated as follows:

**Without the Model (assuming all customers are potential depositors and offering promotions to all):**
- Total promotional cost = 200 x 50 USD = 10,000 USD
- Wasted cost = 100 x 50 USD = 5,000 USD
- Savings = 0 USD

**With the Model (only offering promotions to customers predicted by the model to deposit):**
- Total promotional cost = (78 x 50 USD) + (7 x 50 USD) = 3050 USD + 350 USD = 3,400 USD
- Wasted cost = (100 - (78 + 7)) x 50 USD = 750 USD
- Savings = 10,000 - 3,400 = 6,600 USD

Based on this simple calculation, it is evident that using the classification model to predict the portion of customers likely to deposit allows the company to save a substantial amount of money without sacrificing too many potential depositing customers.

## Rekomendasi
#### Data Analysis
The comprehensive analysis of customer features provides valuable insights for the marketing department to enhance their approach. By identifying the key factors that influence deposit decisions, such as job types, marital status, education levels, and effective communication methods, the marketing team can tailor their strategies to target the right customer segments more effectively. The findings suggest that focusing on personalized and timely interactions, especially through cellular contact and during optimal times like March, can significantly improve deposit acquisition. Moreover, understanding the importance of conversation duration and leveraging past campaign successes can further boost current campaign outcomes. Despite the uncontrollable bank-related features, the customer-centric insights gained from this analysis offer a clear path for the marketing team to increase their success rates in securing deposits.

#### Machine Learning
##### Recommendations for Developers to Improve the Project and Model:

1. Implement policies and input validation systems that encourage every candidate to fill in all required data.
2. Provide input options for missing or zero values.
3. Add new features that might relate to deposits, such as payment information and other customer descriptions.
4. Try other ML algorithms and perform more advanced hyperparameter tuning.
5. Use grid search for selecting the best imputation methods during data cleaning.
6. Analyze data points where the model made incorrect predictions to understand their characteristics, which can then inform feature addition or further feature engineering.

##### Recommendations for Stakeholders or the Company:

1. Increase the number of surveys to collect more and more diverse data.
2. Offer promotions or other strategies that provide incentives to customers to encourage them to make deposits.
3. Based on feature importance, increase cashback incentives for customers who are likely to deposit.
4. Provide promotions for customers with long-distance shipping to reduce deposit-related issues such as high delivery costs or long delivery times.
5. Develop marketing strategies that offer incentives to new customers based on their tenure.

<br/>
Copyright &copy; 2024, Roberto Benedict & Gretty Margaretha.
