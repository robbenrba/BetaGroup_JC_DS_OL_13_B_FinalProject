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

## Conclusion
#### Data Analysis

In our data analysis, we focused exclusively on customer features to better understand their behavior and improve marketing strategies. The analysis explored various dimensions such as job types, marital status, education levels, credit defaults, housing and personal loans, contact communication methods, and timing of marketing efforts. We found that customers with different job types, marital statuses, and education levels show varying tendencies towards making deposits. For instance, single customers and those with professional education are more likely to make deposits. Interestingly, the presence of housing loans does not significantly influence deposit decisions, while personal loans are more common among customers. Effective marketing is facilitated through cellular contact and is most successful when conducted from Tuesday to Thursday. Seasonal trends also play a role, with March being a particularly effective month for securing deposits. Additionally, older customers, especially those in their 60s, are more likely to save in term deposits due to their stable financial situations. The analysis also highlighted the importance of the duration of contact and the positive influence of past campaign successes on current outcomes. However, it is crucial to note that certain high correlations among bank-related features, such as employment variation rate and consumer price index, are beyond the control of the marketing team.


#### Machine Learning

Based on the classification report results from the model, it can be concluded that if the model is used to predict which customers will subscribe to a term deposit, the model can correctly identify 93% of the customers who will not subscribe, allowing the company to focus promotional costs only on potential subscribers, or even eliminate the cost for non-subscribers entirely. The model captures 72% of the customers who will subscribe out of all the actual subscribers based on recall.

The model has a precision of 38% for predicting customers who will subscribe. This means that each time the model predicts a customer will subscribe, there is approximately a 38% chance the prediction is correct. Therefore, there are still false positives, or customers who are predicted to subscribe but actually will not, amounting to 15% of all customers who will not subscribe based on recall.

Assuming the promotional cost per customer is 50 USD and the number of customers in a certain period is 7,647 (6,796 non-subscribers + 851 subscribers), the business case can be calculated as follows:

**Without the Model (all customers are considered potential subscribers and offered the promotion):**
- Total Promotional Cost = 7,647 x 50 USD = 382,350 USD
- Wasted Cost (on non-subscribers) = 6,796 x 50 USD = 339,800 USD
- Total Savings = 0 USD

**With the Model (only customers predicted to subscribe are checked and offered the promotion):**
- Total Promotional Cost = (613 x 50 USD) + (1,018 x 50 USD) = 30,650 USD + 50,900 USD = 81,550 USD
- Wasted Cost (on non-subscribers predicted to subscribe) = 1,018 x 50 USD = 50,900 USD
- Total Savings = 382,350 USD - 81,550 USD = 300,800 USD

Based on this simple calculation example, it is evident that using a classification model to predict the likelihood of customer subscription can significantly reduce costs without sacrificing too many potential subscribers.

## Rekomendasi
#### Data Analysis
The comprehensive analysis of customer features provides valuable insights for the marketing department to enhance their approach. By identifying the key factors that influence deposit decisions, such as job types, marital status, education levels, and effective communication methods, the marketing team can tailor their strategies to target the right customer segments more effectively. The findings suggest that focusing on personalized and timely interactions, especially through cellular contact and during optimal times like March, can significantly improve deposit acquisition. Moreover, understanding the importance of conversation duration and leveraging past campaign successes can further boost current campaign outcomes. Despite the uncontrollable bank-related features, the customer-centric insights gained from this analysis offer a clear path for the marketing team to increase their success rates in securing deposits.

#### Machine Learning
##### Steps Developers Can Take to Improve the Project and Model:

1. Implement policies and input validation systems that encourage each candidate to fill in all required data.
2. Provide input options for missing or zero values.
3. Add new features that could be related to bank term deposit subscriptions, such as payment information and other customer-related details.
4. Experiment with other ML algorithms and perform more advanced hyperparameter tuning.
5. Try grid search for imputation methods during data cleaning.
6. Analyze data points that the model misclassifies to understand their characteristics, which can be used to enhance feature engineering.

##### Recommendations for Data:

1. Collect more diverse and comprehensive data to improve model accuracy.
2. Ensure data is up-to-date and relevant to current market conditions.

##### Recommendations for Users and Stakeholders, **Bank Marketing Division**:

1. Conduct more surveys to gather a larger and more diverse dataset.
2. Offer promotions or other incentives to customers to encourage term deposit subscriptions.
3. Based on feature importance, consider enhancing cashback offers for customers likely to subscribe to term deposits.
4. Provide special promotions for customers with specific needs or preferences, such as those requiring high deposit amounts, to encourage subscriptions.
5. Use customer tenure to create marketing strategies that incentivize new customers to open term deposits.

##### Updated Business Case Calculation

**Without the Model (all customers are considered potential subscribers and offered the promotion):**
- Total Promotional Cost = 7,647 x 50 USD = 382,350 USD
- Wasted Cost (on non-subscribers) = 6,796 x 50 USD = 339,800 USD
- Total Savings = 0 USD

**With the Model (only customers predicted to subscribe are checked and offered the promotion):**
- Total Promotional Cost = (613 x 50 USD) + (1,018 x 50 USD) = 30,650 USD + 50,900 USD = 81,550 USD
- Wasted Cost (on non-subscribers predicted to subscribe) = 1,018 x 50 USD = 50,900 USD
- Total Savings = 382,350 USD - 81,550 USD = 300,800 USD

By utilizing a classification model to predict which customers will subscribe to term deposits, the company can significantly reduce promotional costs while maintaining a high accuracy of targeting potential subscribers.

<br/>
Copyright &copy; 2024, Roberto Benedict & Gretty Margaretha.
