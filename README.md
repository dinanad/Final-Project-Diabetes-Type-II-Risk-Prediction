# Final-Project-Diabetes-Type-II-Risk-Prediction

This final project is one of the requirements for graduating from Job Connector Data Science and Machine Learning Purwadhika Start-up and Coding School. 

Type 2 diabetes is a chronic diseases that lead to death in the United States. Diabetes condition that affects the way the body metabolizes glucose. With type 2 diabetes, the body either resists the effects of insulin or it doesn't produce enough insulin to maintain normal glucose levels. Uncontrolled blood sugar it can cause all sorts of very bad things: infections, damaged kidneys, vision loss, amputations, stroke, medical cost and many more. 

Prediabetes is a precursor condition in which glucose levels are high, but not yet high enough to diagnose diabetes. Almost 90% adults with prediabetes were unaware of their condition. Prediabetes is reversible with lifestyle modification and weight loss, offering an avenue to avoid the adverse effects of diabetes.

Type 2 diabetes needs to be taken seriously and treated. Identifying and predicting these diseases in patients is the first step towards stopping their progression. To treat type 2 diabetes and prediabetes lifestyle changes are very effective, and the side effects of eating more healthfully and staying more active are positive ones.  

There are great benefits to employing data analytics in the health care system to provide insights, augment diagnosis, improve outcomes, and reduce costs. In particular, successful implementation of machine learning enhances the work of medical experts and improves the efficiency of the health care system or assurance. Machine learning models can be useful in the identification of patients with diabetes or prediabetes. There are often many factors that contribute to identifying patients who are at risk for these common diseases. We also consider the prediction of prediabetes and undiagnosed diabetes. In this project I will try to predict case 1: no-diabetes and risk diabetes & case 2: no-diabetes and risk prediabetes/ undiagnose diabetes. In general this project divided into 5 parts.

# 1. Preprocessing Data

This project use data from National Health and Nutrition Examination Surveys 2017 - 2018.
   - Demographic Data
   - Examination Data
   - Laboratory Data
   - Questioner Data
   
   Source Data : https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx
   
The National Health and Nutrition Examination Survey (NHANES) is a program designed by the National Center for Health Statistics (NCHS), which is used to assess the health and nutritional status of the U.S. population. The dataset is unique in the aspect that it combines survey interviews with physical examinations and laboratory tests. NHANES provides insightful data that has made important contributions to people in the United States. It gives important clues to the causes of disease based on the distribution of health problems and risk factors in the population. 

The next step are define target and features, for target use questioner and data laboratory which respondent have diabetes & prediabetes risk. Using the National Health and Nutrition Examination Survey (NHANES) dataset, we search of all available features within the data to develop models for risk diabetes and risk prediabetes detection. After fill missing value in dataset that might be done from remining data, we feature enginnering that may be used for predicting risk diabetes, exploratory data analysis, prepare data for the next stage (case 1 and case 2) and fill missing value head % fat with imputer KNN. 

# 2. Prediction Risk Diabetes (Case I)

  In prediction risk diabetes, Data Biochemistry Profile not include in analysis because objective model. The model will be used for screening so that features are selected based on the ease of filling by user. Check percentage missing value features, association and correlation target with features. This process can help the researcher to find features which will be used in modelling. The next stage is modelling with some algorithm classifier and evalute preformance model.
  
  Seven algorithm machine learning models : logistic regression, support vector machines, random forest, gradient boosting, light gradient boosting, xgboost and adaboost were evaluated on their classification performance. In the following below is the result from recall rate models :

![Recall case 1](https://user-images.githubusercontent.com/69567025/99909475-47fc0e00-2d1b-11eb-80aa-f799bfc37200.png)

   After found four of the best algorithms which are logistic regression, support vector machines, gradient boosting, and adaboost, I tuned hyperparameter for them using GridSearchCV. The results from tuning hyperparameter show that support vector machines gives better learning curve, recall, precision and accuracy. The following below are the parameters that I tuned, confusion matrix and features importance from support vector machines :
   
   Confusion Matrix
   
   ![Confusion Matrix case 1](https://user-images.githubusercontent.com/69567025/99909899-b17d1c00-2d1d-11eb-972c-748bf0c53b87.png)
   
   Fetaures Importance
   
   ![Features Importance case1](https://user-images.githubusercontent.com/69567025/99909935-e38e7e00-2d1d-11eb-9cd5-52d5d55140c2.png)

# 3. Prediction Risk Prediabetes (Case II)

  Prediction risk prediabetes we use all features. Check percentage missing value features, association and correlation target with features. The process same with case 1, we evalute preformance model and choose best model for predicting prediabetes.
  
  Seven algorithm machine learning models : logistic regression, support vector machines, random forest, gradient boosting, light gradient boosting, xgboost and adaboost were evaluated on their classification performance. In the following below is the result from recall rate models :
  
  ![Recall case 2](https://user-images.githubusercontent.com/69567025/99910128-ed64b100-2d1e-11eb-886b-9768914e26e2.png)
  
  After found four of the best algorithms which are logistic regression, support vector machines, random forest, and gradient boosting, I tuned hyperparameter for them using GridSearchCV. The results from tuning hyperparameter show that support vector machines gives better learning curve, recall, precision and accuracy. The following below are the parameters that I tuned, confusion matrix and features importance from support vector machines :
   
   Confusion Matrix
   
   ![Confusion Matrix case 2](https://user-images.githubusercontent.com/69567025/99910218-59471980-2d1f-11eb-9b50-2865d481211f.png)
   
   Fetaures Importance
   
   ![Features Importance case2](https://user-images.githubusercontent.com/69567025/99910248-83004080-2d1f-11eb-948e-a7b5004f2e12.png)

# 4. Dashboard

  From the analysis of existing data and models, a predicting risk diabetes is compiled which consists of 3 parts, namely home, additional test and about Diabetes Risk. In the home section, you can Calculate Risk Diabetes, new data can be analyzed regarding the risk diabetes of user. In additional test, you can Calculate Risk Prediabetes, new data can be analyzed regarding the risk prediabetes of user. In the about section, you can analyze the description risk status by health weight.
  
  ## Home Page:
  
  ![Home page](https://user-images.githubusercontent.com/69567025/99910431-8647fc00-2d20-11eb-9390-7e8bb4783b5c.png)
  
  ## Result prediction risk diabetes
  
  ![Result case1](https://user-images.githubusercontent.com/69567025/99910480-dcb53a80-2d20-11eb-89ec-8afbd526da64.png)
  
  ## Additional test
  
  ![Additional test](https://user-images.githubusercontent.com/69567025/99910556-41709500-2d21-11eb-9c7c-1d859f4939ec.png)
  
  ## Result additional test

![Result case2](https://user-images.githubusercontent.com/69567025/99910689-f905a700-2d21-11eb-8ec6-b90628bc33af.png)

Conclusion : It also allows health planners and government agencies to detect and establish policies, plan research, and health promotion programs to improve present health status and prevent future health problems. Education and prevention programs increasing public awareness, emphasizing diet and exercise were intensified based on the indication of undiagnosed diabetes, overweight prevalence, hypertension, arthritis and cholesterol level figures. Glucose level from biochemistry profile and head % fat is also associated with risk prediabetes.
