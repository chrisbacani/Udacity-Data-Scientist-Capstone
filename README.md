# Udacity Data Scientist Nanodegree Capstone Project
## Customer Service Data Science Engagement; Prediction of Airline Passenger Satisfaction

### Table of Contents
> 1. Abstract
> 2. Dependencies
> 3. Executing Program
> 4. Defined Features and Models
> 5. Author
> 6. Acknowledgements

### 1. Description
Customer satisfaction with airlines has been steadily climibing over the past few years. For many, this problem has been given greater attention in recent years, with the air travel industry restarting after a grinding halt brought about by the COVID-19 pandemic. However, this is a problem that carriers have been facing for years before the pandemic. Uncomfortable seats, crowded flights, delays, and sub-standard amenities are complaints that customers have been airing in recent times. 

Customer satisfaction is something that more and more carriers are paying attention to and striving to improve. Excellent customer service, especially against your competitors is key for marketability, sales, and customer retention. Inveresely - poor customer service ratings can lead to customer attrition and poor company reputation.

As an apprentice for IBM's Client Engineering Data Science Team, I've had the great opportunity to shadow and contribute to different client data science projects. These projects are meant to be a proof of concept for techinical sales, or aimed at solving a new business problem for existing clients. 

This capstone project is aimed at replicating an end-to-end data science project for an airline carrier.

The project process, typically split into three separate work "sprints" consists of:

> Sprint 1 : Data handoff or wrangling, exploratory data analysis
> Sprint 2 : Feature engineering and selection, modeling
> Sprint 3 : Model deployment and explainability (or promotion to IBM Cloud services for further analysis)
    
The end of each "sprint" we conduct a review of the work we did for the client and members of the data science team. The wrap-up of the full engagement is typically followed by a technical review for the fuller IBM community and eminence and advocacy of our work. 

A Medium blog post has been prepared, detailing the work completed for this capstone project. In a data science project, this would typically accompany the wrap-up and advocacy process.

Medium Blog Link: https://medium.com/@chris.bacani7/explaining-airline-passenger-satisfaction-using-interpretable-machine-learning-88d29aa55677


### 2. Dependencies
- Python 3.9+
    - Resource
    - Warnings
    - Pickle
    - Time
- Python Libraries
    - Pandas 1.4.2
    - Numpy 1.21.5
    - Matplotlib 3.5.1
    - Seaborn 0.11.2
- Modeling Libraries
    - Scikit-Learn 1.0.2
        - Preprocessing
        - FeatureSelection
        - Linear : Logistic Regression
        - Tree : Decision tree Classifier
        - Ensemble : AdaBoostClassifier, GradientBoostingClassifier, RandomForestClassifier
        - Neighbors : KNeighborsClassifier
        - NaiveBayes : MultinomialNB, GaussianNB, CategoricalNB
        - Metrics : Accuracy, ROC AUC, Precision, Recall, ROC Curve, Confusion Matrix
    - Extreme Gradient Boosting 1.6.2
    - SHAP 0.41.0
- Data
    - Airline Passenger Satisfaction from [Kaggle](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction?resource=download)

### 3. Execution of Project
File structure of project is shown below. Jupyter notebook is fully executable.

Project
|_ Customer-Satisfaction-Workspace.ipynb
|_ Customer-Satisfaction-Workspace.html
|_ README.md
|_ Data
|	|_ air_train.csv (Training split of data)
|	|_ air_test.csv (Test split of data)
|_ Models
	|_ model_xgb.pkl (Pickled Model, Packaged for Explainability through SHAP)


### 4. Summary of Features, Models, and Results
The target variable ```satisfaction``` was pre-defined in the dataset I obtained from Kaggle.

The following features were used to inform the model:
1.	 Age 
2.	 Gender
3.	 Type of Travel (Business or Pleasure)
4.	 Business Class Travel (Yes or No)
5.	 Economy Plus Class Travel (Yes or No)
6.	 Economy Class Travel (Yes or No)
7.	 Flight Distance
8.	 Time Delayed
9.	 Ease of Booking (Ranked 1 to 5)
10.	 Food and Drink Quality (Ranked 1 to 5)
11.	 Boarding Process (Ranked 1 to 5)
12.	 Seat Comfort (Ranked 1 to 5)
13.	 Inflight Entertainment Quality (Ranked 1 to 5)
14.	 On Board Customer Service (Ranked 1 to 5)
15.	 Leg Room Quality (Ranked 1 to 5)
16.	 Baggage Handling (Ranked 1 to 5)
17.	 Check-In Service (Ranked 1 to 5)

Extreme Gradient Boosting Model (XGBoost) runs with great efficiency (2.05 seconds to completion and 782 MB consumed) and achieves the best peformance across the 10 pipelines tested - with a training accuracy of 95.2 and accuracy of 95.9 on the test data. The model also achieved an ROC AUC Score of 94.9, Precision of 96.1 and Recall of 92.6.

### 5. Author
**Chris Bacani**
*Data Scientist Apprentice; IBM Client Engineering, Data Science and AI Team
Student, Udacity Data Scientist Nanodegree*