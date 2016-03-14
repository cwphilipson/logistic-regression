# logistic-regression
Using logistic regression as a learning algorithm to make predictions

# Summary
Three separate analyses are performed herein: Election Forecasting, Framingham Heart Study, and Healthcare Quality. Each analysis uses data to train a logistic regression model and identify key features for building a predictive model. Data and scripts are described below. These projects were created as a part of the EdX MIT 15071x "The Analytics Edge" course.

## Election Forecasting
This analysis builds a model to predict the state winner of a presidential election based on 3 election years. 
### Data
PollingData.csv  
The data is from RealClearPolitics.com  
Features: State, Year (election year), Republican (1 if Republican won state), Rasmussen (polled data), SurveyUSA (polled data), DiffCount (polls with R winner - Polls with D winner), PropR (polls with R winner / #polls)

### Script
LogisticRegression_ElectionForecasting.Rmd  
The code performs the following steps:  
1.  Import polling data  
2.  Subset data and fill in missing data points using imputation  
3.  Subset data into testing and training data sets
3.  Build a baseline model to generate initial predictions  
4.  Assess correlation and multicollinearity among variables  
5.  Build logistic regression model using different features  
6.  Assess model using test subset and analyze predictions
Output of the code is an html file with model results.  
  
  
## Framingham Heart Study
Analytics to prevent heart disease: identify risk factors, make predictions, validate model, define interventions based on model outcomes. The goal of thte mocel is to predict 10-year risk for coronary heart disease.  
### Data
framingham.csv  
Data is from the Framingham Heart Study and includes 5,209 patients  
Features: male, age (in years), education (some high school [1], high school/GED [2], some college/vocational school [3], college [4]), currentSpoker, cigsPerDay (cigarettes), BP meds (blood pressure medication), prevalentStroke (previous stroke), prevalentHyp (currently high blood pressure), diabetes, totChol (total cholesterol mg/dL), sysBP (systolic blood pressure), diaBP (diastolic blood pressure), BMI (body mass index weight in kg/height m^2), heartRate, glucose (glood glucose level)
### Script
LogisticRegression_FramingamHeartStudy.Rmd  
The code performs the following output:  
1.  Import data  
2.  Split data into train and test sets (use set.seed for reproducibility)  
3.  Build a logistic regression model  
4.  Evaluate predictive power on test set  
5.  Quantify model accuracy  
6.  Evaluate model strength on test set using ROCR and area under the curve  
Output of the code is an html file with model results.  
  
  
## Healthcare Quality
This analysis builds a logistic regrssion model as a healthcare quality assessment using electronically available claims data. 
### Data
quality.csv  
The data is a large health insurance claims database from the EdX MIT 15071x "The Analytics Edge" course. 131 diabetes patients were randomly selected (ages 35-55 from Sep 1, 2003 - Aug 31, 2005).  
Features: MemberID, InpatientDat, ERVisits, OfficeVisits, DaysSinceLastERVisit, Pain, TotalVisits, ProviderCount, MedicalClaims, ClaimLines, StartedOnCombination, AcuteDrugGapSmall, PoorCare (binary; 1 = poor care)   
### Script
LogisticRegression_Healthcare.Rmd  
The code performs the following steps:  
1.  Import data  
2.  Visualize some of the data to determine if there's a correlation between office visits and narcotics  
3.  Randomly split data into testing and training data sets  
4.  Build a logistic regression model  
5.  Make predictions on the training data set  
6.  Build a confusion matrix with different threshold values  
7.  Calculate sensitivity and specificity of model basd on threshold values  
8.  Use ROC curves to identify best threshold  
9.  Assess model based on area under ROC curve  
Output of the code is an html file with model results.  
