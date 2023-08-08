# Coronary-Heart-Disease-Prediction

### ABSTRACT
This research aims to predict the Coronary Heart Disease (CHD) in people living in the town of Framingham, Massachusetts for the coming 10-years. Here the detailed history of patients is given This study uses Logistic regression, K nearest neighbors and Random forest with and without smote to predict the results. From the study we can conclude that Age, Glucose level, Systolic blood pressure, BMI, Total Cholesterol are the most important reasons for the cause of  coronary heart disease. From the visualizations we can compare how age, Systolic BP, Diastolic BP, and total cholesterol level affects the risk factor to be affected by Coronary Heart Disease in the coming 10 years. In this research paper, we examine the  significant insights in more detail, talk about the study's limitations, and summarize some of the significant conclusions.

### INTRODUCTION
Over 12 million people die each year from cardiac disorders globally, according to the World Health Organization. Cardio Vascular Diseases account for 50% of mortality in the US and many other developed nations. Making decisions about lifestyle changes for high-risk patients can be aided by early detection of cardiovascular diseases, which can also lessen complications. 
This data set corresponds to the ongoing cardiovascular study of people living in the town of Framingham, Massachusetts. The objective is to determine if the patient has a 10-year risk of developing future Coronary Heart Disease (CHD). The dataset that is available has about 4000 records of 15 different parameters and contains patient information. Every characteristic listed here carries a potential risk.

This study focuses on to the predicting the 10-year risk of developing future coronary Heart Disease (CHD). This paper will explore the following research questions:
- What are the top 5 features that cause Cardio Vascular Diseases?
- How does age affect the risk factor?
- What role does Blood Pressure have in predicting the Heart Disease risk?


### METHODOLOGY
	
#### Dataset Description: 

The dataset has about 4000 records of 15 different parameters and contains patient information. The 15 attributes present in the dataset are divided into categorical and continuous variables.

 <img width="396" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/efed4107-d014-4315-93d7-8fc5f6712284">


#### Data Cleaning
Data preprocessing is a phase in the data mining and data analysis process that converts raw data into a format that computers and machine learning algorithms can understand and evaluate. A bad data will result into model that is badly trained and won't be useful for the analysis. Good data which is well preprocessed will lead to accurate solutions. The data cleaning process involves the following steps:
	
#### Handling Missing Values
Various techniques are used to treat with missing values such as removal of the rows that have missing values, imputing the NA/missing values with aggregations like mean, median. For this dataset the columns cigsPerDay, BPMeds, totChol, BMI, heartRate, glucose have missing values. These were imputed with median of corresponding column. The detail about the missing values is represented in the below figure.

<img width="611" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/cedba630-1c9e-4349-b73d-d5607feb7e06">
 
#### Outlier Removal:
The columns tolChol and glucose has significantly higher values. In the totChol (Total Cholesterol) column, the values higher than 500 were removed. Similarly, the glucose values higher than 400 were discarded.
	
#### Removal of unnecessary columns
Among all the columns, education has no effect on whether a person would be in a risk of getting the heart disease or not. In addition, education column has 105 missing values. So, we have discarded the column.
	
 
### Exploratory Data Analysis: 

Exploratory Data Analysis deals with analyzing the variables. It refers to initial investigation of data to discover interpretable patterns from the dataset.
	
#### Correlation Matrix:
 
From the above Correlation Matrix, we can say that sysBP and diaBP have a positive correlation with a strong value of 0.79 and also diaBP and BMI  as well as age and sysBP also have a positive correlation value of 0.39.  

<img width="523" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/d4f1c04e-919c-4fae-9afc-7be0c6bd72d9">


#### Box Plot between Age and 10-Year Risk:
This box plot represents the relation between Age and 10-Year risk. Here the Red box is for “No” and the blue box is for “Yes”.  The line in the middle of box represents the median value. We can see that the median of the blue box is higher than the red. It represents that as the age increases there is a higher risk of having CHD in coming 10 years. 

<img width="620" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/6655fb97-bfe1-4637-8299-65b05e98bd78">
 
#### Box Plot between Systolic BP and Diastolic BP vs 10-Year Risk:
Blood pressure is measured using two numbers, the first one is systolic blood pressure which    measures the pressure when the heart beats and the second one which is diastolic blood pressure measures the pressure when heart rests between beats From the below box plots we can determine that if the systolic BP and Diastolic BP increases the risk of CHD over the next 10 years also increases.  

<img width="593" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/9789d297-e316-4ff1-9494-8f78f7521e7e">

#### Box plot between Total Cholesterol vs 10 Year Risk:
The following box plot represents the relationship between total cholesterol and 10-year risk. From the box plot we can determine that the median of the blue box is slightly higher than the red box. This represents that increase in total cholesterol will increase the risk of Coronary Heart Disease over the next 10 years.

 <img width="591" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/09d7e464-812e-461e-a63e-bafa58177b36">

#### Bar Graph between Cigarettes consumptions vs Age:
The above bar plot represents the relationship between age and frequency of the cigarettes they smoke. It can be seen that people between the age of 35 and 40 years.

<img width="650" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/52c4f386-1893-429a-91f3-bb7bcd2fc503">
 
### MODELING:

The problem we are trying to solve is – predicting whether a person is at a risk of getting an heart disease in the next 10 year span. The modeling algorithms we used are Logistic Regression, K-Nearest Neighbors, Random Forest. For all the models, we used various metrics to calculate the test results. Accuracy is the primary metric. However, relying only on accuracy to validate the model is not ideal. So, we considered Confusion Matrix to derive Precision, Recall and F1 – Score. This is because we tried to reduce Type 1 (False Positives) and Type 2 errors (False Negatives). 

<img width="280" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/1f50e7d3-21af-4340-9e76-4a9c0cf96839">
 
<img width="630" alt="image" src="https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/ed4fe11f-097c-4cc9-9742-a08fa4b6ef46">

#### Logistic Regression: 

Logistic Regression is used when the class variable is binary, such classification is called binary classification. Further, it can also be used for Multi-Class Classification. It is used to explain the relation between one dependent variable(Y) with one or more independent variables (X).

![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/e08bc2f6-7433-44b2-aa37-5bd12c946b0d)

#### K-Nearest Neighbor: 

KNN is a lazy learning algorithm. First, data (of n features) is projected into a n-dimensional space, for a test data point Xq it calculates the distance from this point to all the data points in the training dataset. Based on the value of the K, it gets class label of the top K nearest data points and calculates the maximum votes among all the nearest neighbors and assigns to the test point Xq.

 
![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/11ecebbf-065a-4871-bc80-7f2702a4ddd2)

 
![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/7e0af224-3b9d-41b4-92f1-514bb135bcc9)


#### Random Forest: 

Random Forest uses bagging technique that gives higher accuracy compared to other models and its interpretability is also good. It avoids the problem of overfitting and reduces the variance. 


![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/1c0028e4-3732-4136-bf43-d95684888a1a)


Even though the accuracy of all these models is considerably good, Confusion matrix, Precision, recall values state that the models are generalizing the positive class to negative class. This is because the class labels are imbalanced. To overcome this problem, we need to perform oversampling. Here, we are using Synthetic Minority Oversampling Technique (SMOTE). Initially the data has 3,593 negative records and 643 positive records. After using SMOTE the data is balanced to 3,593 negative records and 3581 positive records.


### MODELING – AFTER SMOTE

We performed similar analysis and model building on the balanced data. Below are the tabulated results comprising Confusion Matrix, Accuracy, Precision, Recall and F1-Score values.
 
![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/6122cada-aa1c-4bef-bc7b-a7209477b700)


Comparing and Contrasting above results: For Logistic Regression


![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/fe09c011-d610-4f8c-89c7-ca081c141fc3)


 ![image](https://github.com/sowmya-chakravarthy/Coronary-Heart-Disease-Prediction/assets/120443811/85549538-50ee-43ff-ade8-023a127e15d6)


### LIMITATIONS AND FUTURE ANALYSIS NEEDED:

The dataset available is an imbalanced data so there was an issue of introducing bias to the training model. If the data is balanced then we could have more information about the people of positive class. 

The amount of data is not large enough and it would have been more beneficial if wide range of data would be available and many other regions of people were included and not limiting to a particular place or region. Food Habits and workout pattern also play a crucial role in predicting the Coronary Heart Disease (CHD). 

### CONCLUSION:

In conclusion, this research attempted to produce few insights on the top five important reasons for the cause of Coronary Heart Disease. It determines that Random forest with SMOTE is the best model to derive the important features with the best accuracy among all. Based on the findings, precautions might be taken against those who are anticipated to have a high risk of developing coronary heart disease.

### REFERENCES
Draelos, A. R., Draelos, P. by R., Draelos, R., I have an MD and a PhD in Computer Science from Duke University.) Measuring performance: The confusion matrix. Glass Box. Retrieved December 7, 2022, from https://glassboxmedicine.com/2019/02/17/measuring-performance-the-confusion-matrix/n 
