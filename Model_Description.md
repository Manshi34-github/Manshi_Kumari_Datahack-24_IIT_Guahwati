# Manshi_Kumari_Datahack-24_IIT_Guahwati

Explanation of Method and Approach

Step_1. Loading Data:

  I started by loading the provided datasets: training features, training labels, and test features.

Step_2. Preparing the Data:

  I identified which columns are numerical and which are categorical.
  Some categorical columns have a natural order (like levels of concern or knowledge), so we treat them as ordinal features.

Step_3. Handling Missing Values and Scaling Data:
  
  For numerical data, we fill in missing values with the median and scale the values to have a standard range.
  For ordinal data, we fill in missing values with the most common value and then encode the values to numbers based on their order.
  For other categorical data, we also fill in missing values with the most common value and then convert the categories to one-hot encoding (a way of representing 
  categorical data).
  
Step_4. Combining Preprocessing Steps:

  I have used a ColumnTransformer to apply the appropriate preprocessing steps to each type of data (numerical, ordinal, and categorical).

Step_5. Splitting the Data:

  I splited the training data into a training set and a validation set to evaluate our model's performance.

Step_6. Training the Model:

  I have used a logistic regression model that can handle multiple target variables (whether someone got the xyz vaccine and whether they got the seasonal flu 
  vaccine).
  I have created a pipeline that first preprocesses the data and then trains the model.
 
Step_7. Making Predictions:

  I have used the trained model to predict the probabilities that each person in the test set received each vaccine.
  I rounded these probabilities to one decimal place for submission.

Step_8. Creating and Saving Submission Files:

  Finally, I have created a submission file in the required format with respondent ID, and the predicted probabilities for the xyz and seasonal vaccines.
  Then saved this submission file both as a CSV and as an Excel file.
  This approach ensures that the data is properly prepared and missing values are handled before training the model. It also uses appropriate methods to handle 
  different types of data and provides predictions in the required format for submission.






