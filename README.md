# CIND-820-Big-Data-Analytics-Project

The objective of this big data analytics project is to identify the key variables that predict long-term outcomes of adult U.S. residents who developed COVID-19 before February 2023. Behavioural Risk Factor Surveillance System (BRFSS) data is collected annually by the U.S. Centers of Disease Control and Prevention; residents of the 50 states, the District of Columbia, Guam, Puerto Rico, and the Virigin Islands participate in telephone surveys. BRFSS survey data which was collected between January 2022 and February 2023 will be used to investigate the following three research questions:  

    1.	What are the key predictors of long COVID symptoms? 
    2.	Among people who tested positive for COVID-19, what variables predict frequent mental distress?  
    3.	What factors predict cognitive difficulty among people who have contracted COVID-19? 

The primary outcome variables of interest are <b> COVIDSMP </b>, <b> MENTHLTH </b>, and <b> DECIDE </b>, which represent the answers to the questions <i>Did you have any symptoms lasting 3 months or longer that you did not have prior to having coronavirus or COVID-19? </i>, <i>Now thinking about your mental health, which includes stress, depression, and problems with emotions, for how many days during the past 30 days was your mental health not good?</i>, and <i> Because of a physical, mental, or emotional condition, do you have serious difficulty concentrating, remembering, or making decisions? </i>, respectively. The <b> MENTHLTH </b> variable will be dichotimized using a threshold of 14 days, as 14 or more days of mentally unhealthy days is commonly used as a measure of frequent mental distress, which is associated with mental disorders. 

<b>Content of the Repository: </b> <br>
<b>1. Exploratory Data Analysis folder:</b> <br>
    * Contains the EDA report (minimal version as an .html file, full version compressed as a .zip file)  <br>
    * The Python code that was used to generate the EDA report in an .ipynb file <br>
    * The codebook for the BRFSS dataset as an .html file <br>
    * Direct links to the .html files 

<b>2. HTML Files folder: </b> <br>
    *Contains all .ipynb files converted to .html format 

<b>3. Python Notebooks folder:</b>
   * The 'Initial Data Preparation' python notebook, which contains the code to clean the BRFSS dataset for analysis <br>
     
 <b>Folders for research question one, two, and three, each of which contain: </b>
        * The "Train_Test_Split" notebook, which contains the code to split the BRFSS dataset into training/validation and test sets 
        * The "Removing_low_variance_&_high_missing_data_attributes" notebook, which contains the code to remove low variance attributes and attributes with over 10% missing data 
        * The "Splitting_Data_for_Sliding_Window_Cross_Validation" notebook, which contains the code to split the data for sliding window validation (the dataset was split five-fold)
        * The "Sliding Window 1" to "Sliding Window 5" notebooks, which illustrate the processes of imputing the data, standardizing the data, generating dummy variables, addressing multicollinearity issues, using the SMOTE algorithm, and
           generating logistic regression, Naive Bayes, random forest, and LightGBM models for each of the five sliding windows respectively. 
        * The 'Grid_Search_Results' notebook, which contains the code to combine the F2-scores from each of the five sliding windows and to choose the optimal model hyperparameters. 
        * The 'Evaluating_models_using_test_data' notebook, which contains the steps executed to evaluate model performance on the test data set <br>
    
<b> 4. Working Dataset folder: </b> <br> 
    * Contains the working dataset as both .csv and pickle files 



