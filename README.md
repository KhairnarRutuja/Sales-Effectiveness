# DATA SCIENCE PROJECT REPORT ON SALES EFFECTIVENESS
## BUSINESS CASE:- BASED ON THE GIVEN FEATURE OF DATASET WE NEED TO PREDICT THE PROSPECTIVE LEAD CATEGORY, DISTINGUISHING BETWEEN 'HIGH POTENTIAL AND 'LOW POTENTIAL' CUSTOMERS.

## INTRODUCTION OF PROJECT
FicZon Inc, a prominent IT solution provider offering a spectrum of products from on-premises solutions to SAAS-based offerings, relies heavily on its digital channels, especially the website, for lead generation. However, the company faces a pivotal challenge in sustaining sales effectiveness amidst a maturing market landscape and increased market entrants, leading to a noticeable downturn in sales performance. The pivotal factor influencing effective sales lies in the quality of leads, predominantly determined by manual categorization heavily reliant on the sales team's judgment.
While FicZon maintains a quality process for ongoing lead categorization, its primary value lies post-analysis, offering insights rather than immediate conversation strategies. Recognizing the critical role of lead quality in sales efficacy, FicZon seeks to delve into Machine Learning methodologies. The objective is to proactively categorize lead quality using predictive models, aiming to significantly augment sales effectiveness by transitioning from subjective, human-dependent categorization to data-driven, predictive lead quality assessment.

### ABSTRACT:
This project revolves around the integration of Machine Learning into FicZon Inc's lead management system to pre-categorize lead quality and elevate sales performance. Currently facing a decline in sales due to market maturation and intensified competition, FicZon aims to alleviate this challenge by harnessing ML's predictive capabilities. The objective is to transition from manual lead categorization, heavily reliant on sales staff, to a proactive ML-driven approach that anticipates lead quality. By pre-determining lead quality, FicZon anticipates a considerable boost in sales effectiveness, optimizing resource allocation and refining marketing strategies for improved outcomes.
Methodology involves data preprocessing, exploratory data analysis (EDA), feature engineering, and the application of machine learning algorithms Through this methodology, FicZon aims to revolutionize its lead management process, transitioning from subjective manual categorization to a data-driven ML approach. This transformation is anticipated to drive substantial improvements in sales effectiveness, facilitating more informed decision-making and propelling FicZon towards sustained growth and success.

### DEVICE PROJECT IN-TO MULTIPLE STEPS:
1.	Data Collection 
2.	2.Loading data
3.	3.Domain Analysis 
4.	4.Basic Checks of data
5.	EDA (Univariate Data Analysis)
6.	Data Pre-processing 
7.	Feature Selection 
8.	Building ML Model
9.	Training & Model Evaluation
10.	Model Saving

### LOADING DATA:
load data in python using panda’s library

### DOMAIN ANALYSIS:
•	Understanding the meaning of each feature and grasping the significance of every attribute in defining sales effectiveness is essential. Status is the target Variable Represents the current status of the transaction or order.

**1. CREATED:-**
- This column likely represents the date or timestamp when the record was created or the transaction occurred.

**2. PRODUCT_ID:-**
- An identifier for the specific product being sold or referenced.

**3. SOURCE:-**
- Indicates the origin or channel through which the product was acquired or sold. This could be online, offline, referrals, etc.

**4. MOBILE:-**
- Possibly denotes a mobile number associated with the transaction or customer.

**5. EMAIL:-**
- Represents the email address related to the transaction or customer.

**6. SALES_AGENT:-**
- Refers to the person responsible for making the sale or handling the transaction.

**7. LOCATION:-**
- Indicates the geographical location or address associated with the transaction, likely where the product is delivered or the customer is located.

**8. DELIVARY_MODE:-**
- Specifies the method or mode of delivery for the product—whether it's digitally delivered.
- **Mode1, Mode2, Mode3, Mode4, Mode5** could stand for various delivery options or methods. 

**9. STATUS:-**
- Represents the current status of the transaction or order. 
- This could include

**1. JUST ENQUIRY:-**
- Represents leads that are inquiring but haven't progressed further in the sales funnel.

**2. POTENTIAL:-**
- Likely signifies leads that have potential for conversion but haven't reached that stage yet.

**3. LONG TERM:-**
- Represents leads that might convert in the long run but are not immediate prospects.

**4. IN PROGRESS POSITIVE:-**
- Indicates leads that are actively progressing towards a positive conversion.

**5. IN PROGRESS NEGATIVE:-**
- Represents leads that are progressing but might not result in a successful conversion.

**6. LOST:-**
- Denotes leads that were pursued but eventually lost or did not convert.

**7. OPEN:-**
- Possibly represents leads that are still being actively worked on but haven't progressed significantly.

### EDA (UNIVARIATE, BIVARIATE, MULTIVARIATE DATA ANALYSIS)
I.	UNIVARIATE DATA ANALYSIS
- In nivariate analysis, we get the Minimum, Maximum, Some statistical information of the particular feature.

**Note:-**
Due to the absence of numerical features and also lots of categories are present in categorical feature, bivariate and multivariate analysis are not feasible.

### DATA PREPROCESSING
•	First, we check the missing values, In this data, there is few feature have missing values present.
•	Product-ID, Source, Mobile, Sales_Agent, Location have missing values present in these features. 
•	Handle Missing values in categorical data can be handled by imputing them with the mode, which represents the most frequently occurring value within the respective categorical feature.
•	Second, features is contain lots of different label so we compresses and merged the label 
•	I Handle categorical data and use frequency encoding. Because features have contained lots of label.

### FEATURE ENGINEERING
•	First we drop unique and constant feature there are three unique feature such as Created, Mobile, EMAIL.
•	Before check correlation changing data type after that Check the correlation with the help of heatmap and seen the from the above heatmap I analyzing the heatmap, it appears that there are no highly correlated features present. Therefore, we do not drop any feature based on correlation.
•	I haven't addressed duplicates as I've compressed and merged labels, ensuring the dataset doesn't contain any duplicates due to label transformations
•	After that save & load the preprocess data, Save the dataframe to a CSV file.

### MODEL CREATION & EVALUATION
•	Define Independent and dependant variable and split the data into training and testing.
•	For Training 80% & Testing 20% data
•	I check data is balanced or not after check the data has imbalanced so I utilized the SMOTE technique to balance the data.
•	Use classification algorithm algorithms including Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost, KNN, Bagging and Artificial Neural Network (ANN).
•	Afterward, I evaluated the models using accuracy, recall, precision, and F1 score metrics.

### BEST MODEL
•	Our best performed model with accuracy (0.72) metric is XG Boost. This classifier could achieve accuracy rate 0.72 that is average accuracy.

### MODEL SAVING 
•	Save the model using pickle file.

### CONCLUSION
•	 In a project focused on improving sales by identifying high-quality leads, various machine learning models were tested using a dataset. The goal was to find the most effective model based on different performance measures like Accuracy, Recall, Precision, and F1 scores.
•	After evaluating these models, it was determined that the XG Boosting outperformed the others by achieving the highest accuracy score. This suggests that, compared to the other models tested, XG Boosting was most successful in accurately predicting lead quality, making it the top performer for this particular task.


