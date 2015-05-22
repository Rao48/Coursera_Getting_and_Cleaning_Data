# Coursera_Getting_and_Cleaning_Data
Course Project
This repository hosts the R code and documentation files for the Data Science's course Getting and Cleaning data, offered in coursera.
The UCI Human Activity Recognition (HAR) Using Smartphones dateset files is used in this analysis.
The code assumes that data is in the same folder (UCI HAR Dataset), un-compressed and without names altered.
The CodeBook.md briefly explains the variables, the data, and any changes or work that was dome to clean up the data.
The run_analysis.R code has all the codes to initiate and complete the analysis described in these five steps; 

1.	Merges the training and the test sets to create one data set.
2.	Extracts only the measurements on the mean and standard deviation for each measurement. 
3.	Uses descriptive activity names to name the activities in the data set
4.	Appropriately labels the data set with descriptive variable names. 
5.	From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

This analysis code can be sourced in RStudio via the folder setwd("~/Rspace/UCI HAR Dataset"). The UCI HAR Dataset folder contains; test, train, activity_labels.txt, features.txt, features_info.txt, README.txt and tidyData.txt files.
The result of the fifth step is called mean_data.txt, it has been uploaded in the course project page.
