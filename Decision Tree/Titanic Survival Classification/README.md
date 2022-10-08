Predict whether a passenger from the titanic would survive based on selected features.

We do not require the features Passenger, Name, SibSP, Parch, Ticket Cabin, Embarked for the classification.

Predict survival based on the remaining features.

Steps:

1. Drop unwanted features.
2. Check for NULL values. Since the feature the contains NULL values is 'Age' (numeric), we can fill the NULL values with the mean.
3. Encode categorical features.
4. Separate Input and Output data.
5. Split training and testing data.
6. Train and test the model using training and testing data. 
