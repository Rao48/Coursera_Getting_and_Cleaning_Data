Brief Introduction:
The code run_analysis.R performs the five steps explained in the course project's introduction.
- First step, all the related data is merged using the rbind() function. By related, we look into those files having the same 
number of columns and referring to the same entities. 
- Next, only those columns with the mean and standard deviation measures are picked from the whole dataset. 
After extracting these columns, they are given the correct names, taken from features.txt. 
-An activity data is addressed with values 1:6, the activity names and IDs from activity_labels.txt are taken and they 
are substituted in the dataset. 
-	In the entire dataset, those columns with unclear column names are corrected. 
-	Lastly, we generate a new dataset with all the average measures for each subject and activity type 
(30 subjects * 6 activities = 180 rows). The output file is called averages_data.txt, and uploaded to this repository. 

The Variables:
-	x_train, y_train, x_test, y_test, subject_train and subject_test have the data from the downloaded files. 
-	x_data, y_data and subject_data merge the previous datasets for further analysis. 
-	Features contains the right names for the x_data dataset, which are applied to the column names stored in 
mean_and_std_features, a numeric vector used to extract the desired data. 
-	A similar approach is taken with activity names through the activities variable. 
- All_data merges x_data, y_data and subject_data in a big dataset. 
-	Lastlly, averages_data contains the relevant averages which will be later stored in a .txt file. ddply(), 
plyr package is used to apply colMeans() and to make analysis easier.
