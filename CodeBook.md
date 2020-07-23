Getting and Cleaning Data Course Project CodeBook
=================================================

Data source
-----------
The dataset is derived from the [Human Activity Recognition Using Smartphones Data Set](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

Feature Selection 
-----------------
The README and features.txt files in the original dataset tell us about the feature selection for the dataset.

The set of variables that are estimated (and kept for this assignment) from those original signals are: 

* mean(): Mean value
* std(): Standard deviation

Data Processing
---------------
The run_analysis.R script performs the following steps to clean the data:
- read X_train.txt, y_train.txt and subject_train.txt from the "./data/train" folder and store them in trainData, trainLabel and trainSubject variables respectively.
- read X_test.txt, y_test.txt and subject_test.txt from the "./data/test" folder and store them in testData, testLabel and testsubject variables respectively.
- Concatenate testData and trainData to generate a data frame called joinData; concatenate testLabel and trainLabel to generate a data frame called joinLabel; concatenate testSubject and trainSubject to generate a data frame called joinSubject.
- read the features.txt file from the "/data" folder and store the feature data in a variable called features. To extract the measurements on the mean and standard deviation, we get a 66 indices list and then subset joinData with the 66 corresponding columns.
- clean the feature names by removing the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.
- read the activity_labels.txt file from the "./data"" folder and store the data in a variable called activity.
- clean the activity names by making all names to lower cases. If the name has an underscore between letters, we remove the underscore and capitalize the letter immediately after the underscore.
- transform the values of joinLabel according to the activity data frame.
- combine the joinSubject, joinLabel and joinData by column to get a new cleaned data frame called cleanedData. Properly name the first two columns, "subject" and "activity". 
- write the cleanedData out to "merged_data.txt" file in current working directory.
- generate a second independent tidy data set with the average of each measurement for each activity and each subject.
- write the result out to "data_with_means.txt" file in current working directory.