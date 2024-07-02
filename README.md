# CIND-820-Big-Data-Analytics-Project

The objective of this big data analytics project is to identify the key variables that predict long-term outcomes of adult U.S. residents who developed COVID-19 before February 2023. Behavioural Risk Factor Surveillance System (BRFSS) data is collected annually by the U.S. Centers of Disease Control and Prevention; residents of the 50 states, the District of Columbia, Guam, Puerto Rico, and the Virigin Islands participate in telephone surveys. BRFSS survey data which was collected between January 2022 and February 2023 will be used to investigate the following three research questions:  

    1.	What factors predict symptoms lasting three months or longer following a COVID-19 infection? 
    2.	Among people who tested positive for COVID-19, what key variables predict frequent mental distress? 
    3.	What factors predict serious difficulty concentrating, remembering, or making decisions among people who have been infected with COVID-19? 

The primary outcome variables of interest are <b> COVIDSMP </b>, <b> MENTHLTH </b>, and <b> DECIDE </b>, which represent the answers to the questions <i>Did you have any symptoms lasting 3 months or longer that you did not have prior to having coronavirus or COVID-19? </i>, <i>Now thinking about your mental health, which includes stress, depression, and problems with emotions, for how many days during the past 30 days was your mental health not good?</i>, and <i> Because of a physical, mental, or emotional condition, do you have serious difficulty concentrating, remembering, or making decisions? </i>, respectively. The <b> MENTHLTH </b> variable will be dichotimized using a threshold of 14 days, as 14 or more days of mentally unhealthy days is commonly used as a measure of frequent mental distress, which is associated with mental disorders. 

<b>Current State of the Project: </b>
1. The initial exploratory data analysis has been conducted, and an EDA report has been generated
2. The BRFSS dataset has been cleaned; all attributes have been converted to the appropriate data type and missing values have been correctly encoded.
3. <b>Research question one: </b>
   * The data has been split into the training/validation set and the test set 
   * Zero variance attributes and attributes with over 10% missing data have been removed from the dataset 
   * The training/validation dataset has been split five-fold for the sliding window validation 
   * Missing data was imputed, standardization of numeric variables was performed, multicollinearity was assessed using VIF values and highly correlated variables were addressed, and the SMOTE algorithm was applied to address imbalanced
    data 
   * Four machine learning algorithms were run on each sliding window; logistic regression, naive bayes, random forest, and gradient-boosted trees. Grid search was used to optimize model hyperparameters; the F2-score was the metric
    employed. 
   * Each of the four models was run on the test data set. Confusion matrices were generated, and the model with the highest F2-score was identified. 

* The F2-score is currently quite low (apprx. 49%); measures to improve this metric will be investigated. <br>
* This process will be repeated for both research question two and research question three. 

<b>Content of the Repository: </b> <br>
<b>1. Exploratory Data Analysis folder:</b> <br>
        * Contains the EDA report (minimal version as an .html file, full version compressed as a .zip file)  <br>
        * The Python code that was used to generate the EDA report in an .ipynb file <br>
        * The codebook for the BRFSS dataset as an .html file <br>
        * Direct links to the .html files 

<b>2. Initial Code folder:</b>
   * The 'Initial Data Preparation' python notebook, which contains the code to clean the BRFSS dataset for analysis <br> 
    <b>Research Question One folder: </b>
        * The "Train_Test_Split" notebook, which contains the code to split the BRFSS dataset into training/validation and test sets 
        * The "Removing_low_variance_&_high_missing_data_attributes" notebook, which contains the code to remove low variance attributes and attributes with over 10% missing data 
        * The "Splitting_Data_for_Sliding_Window_Cross_Validation" notebook, which contains the code to split the data for sliding window validation (the dataset was split five-fold)
        * The "Sliding Window 1" to "Sliding Window 5" notebooks, which illustrate the processes of imputing the data, standardizing the data, generating dummy variables, addressing multicollinearity issues, using the SMOTE algorithm, and
           generating logistic regression, Naive Bayes, random forest, and gradient-boosted tree models for each of the five sliding windows respectively. 
        * The 'Grid_Search_Results' notebook, which contains the code to combine the F2-scores from each of the five sliding windows and to choose the optimal model hyperparameters. 
        * The 'Evaluating_models_using_test_data' notebook, which contains the steps executed to evaluate model performance on the test data set 
    HTML Files folder:
        * Contains the .ipynb files converted to .html 



