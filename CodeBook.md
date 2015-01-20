---
title: "CodeBook"
output: html_document
---
### Variable list and descriptions

-ActivityTest, ActivityTrain, SubjectTrain, SubjectTest, FeaturesTest, FeaturesTrain are contrain the data from the downloaded files.

-dataSubject, dataActivity, and dataFeatures combines the respective training and tes data.

-data is a column bined of dataFeatures, dataSubject and dataActivity.   

-subFeaturesNames, selectedNames, and Data Subests data to contain mean or standard deviation of variables.

-activityLabels and dataActivity name activities in the dataset.

###Data

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. 

###Transformation


####1. Merges the training and the test sets to create one data set.
Used rbind and cbind to combine training and test sets

####2. Extracts only the measurements on the mean and standard deviation for each measurement. 
Use grep and subset to extract only the measurements on the mean and standard deviation for each measurement

####3. Uses descriptive activity names to name the activities in the data set
Used activity label file to rename the activities

####4. Appropriately labels the data set with descriptive variable names. 
Used names() to provide more descriptive variable names 

####5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Used plyr package to aggregate and order the data. Created a final tidy dataset.


