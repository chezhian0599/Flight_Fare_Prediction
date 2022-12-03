# Flight_Fare_Prediction

## Objective:

- The objective is to develop a web application using Python,Flask Framework that uses a machine learning model to predict the **“Flight Fare”** 
   based on the various input given by the user.
 - Deploy the developed Web application using Heroku.
 
 ## Methodology:
 
 - The data used for developing Machine Learning model is provided by Technocolabs for  this Internship.

- With the collected data the steps performed are:
     - Perform Data Cleaning.
     - Perform Exploratory Data Analysis (EDA) on the data.
     - Variable/Feature Selection on the given dataset.
     - Develop a Machine Learning model to predict the Flight Fare 
     - With the model developed, create a web application using  Flask Framework .
     - Deploy the created web application using Heroku.

## Data Selection:

- The dataset Provided by Technocolabs had 11 features (10 object datatype, one integer datatype) and 13356 records.

- Since the Data is not in a required form to create Machine Learning Model, 
  it will be pre-processed and made to the correct form.
  
## List of Variables:

 1. Airline 
 2. Date of Journey 
 3. Source
 4. Destination
 5. Route
 6. Dep-Time
 7. Arrival-Time
 8. Duration 
 9. Total-Stops
 10. Additional-info 
 11. Price
 
 ## Data Pre-Processing for Training Set:
 
 ### Date of Journey Column :

- With the help of the Datetime Function in Python, Journey day & Journey month are extracted.   
- Two new columns, Journey-day, Journey-month created.
- Then the Date of Journey Column is Dropped.

### Dep-Time Column :

- With the help of the Datetime Function in Python, Journey hour & Journey minute are extracted.
- Two new columns, Dep-hour, Dep-min created.
- Then the Dep-Time Column is Dropped.

### Arrival-Time :

- With the help of the Datetime Function in Python, Arrival hour & Arrival minute are extracted.
- Two new columns, Arrival-hour, Arrival-min created.
- Then the Arrival-Time Column is Dropped.

### Duration Column:
- Extracting Hours and Minutes from Duration and Saving it in Duration_hours and Duration_mins columns.
 Then the Duration column is Dropped.

### Airline Column (Nominal Data) :
- As Airline is Nominal Categorical data, OneHotEncoding is performed .

### Source Column (Nominal Data) :
- As Source is Nominal Categorical data OneHotEncoding is performed.

### Destination Column (Nominal Data) :
- As Destination is Nominal Categorical data OneHotEncoding is performed.

### Dropping Unwanted Columns :
- Route and additional_info columns were dropped.

### Total_stops Column (Ordinal Data) :
- As this is the Ordinal Categorical data, we perform LabelEncoder.

### Concatenation :
- Concatenating processed  train_data, Airline, Source, and Destination columns to our dataset and dropping the unprocessed columns.




## The steps Performed for the training set is performed on the test set as well.

- Here the preprocessing steps are carried out separately for training set and test set to avoid data leakage . 
- It will affect the accuracy of our model.For that reason we are performing this step separately.

## Feature Selection:
- Feature Selection is the method of reducing the input variable to your model by using only relevant data and eliminating noise in data.
- It is the process of automatically choosing relevant features for your machine-learning model based on the type of problem you are trying to solve

## Model Building:

### After all processing steps, models are built using 
- Linear Regression
- Xgboost Regression
- Random Forest Regression

## Note:
- Among all these algorithms, Random Forest Regressor has high Accuracy. 
- So hyperparameter tuning is done to improve its accuracy further.

## Conclusion:
- I have created a web app using flask.
### Template Design :
- The User Interface for the web application is developed using HTML. 
- The page is designed in such a way the information about the features can be passed to the backend .

### Backend:
- The Backend for the web application is done using Flask Frame Work.
- Flask is a web development framework developed in Python.



## Deployment:
- Deployed it in Heroku.






     
   




	




