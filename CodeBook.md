The dataset was downloaded from Human Activity Recognition Using Smartphones Data Set. Abstract: Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors. The download has two options; Data folder and Data Set description.
Abstract: Human Activity Recognition database built from the recordings of 30 subjects performing activities of daily living (ADL) while carrying a waist-mounted smartphone with embedded inertial sensors.	
Data Set Characteristics:  	Multivariate, Time-Series	Number of Instances:	10299	Area:	Computer
Attribute Characteristics:	N/A	Number of Attributes:	561	Date Donated	2012-12-10
Associated Tasks:	Classification, Clustering	Missing Values?	N/A	Number of Web Hits:	185905

Data Set Information:
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
Check the README.txt file for further details about this dataset. 

A video of the experiment including an example of the 6 recorded activities with one of the participants can be seen in the following link: [Web Link]
Attribute Information:
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.
Source:
Jorge L. Reyes-Ortiz(1,2), Davide Anguita(1), Alessandro Ghio(1), Luca Oneto(1) and Xavier Parra(2)
1 - Smartlab - Non-Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova, Genoa (I-16145), Italy. 
2 - CETpD - Technical Research Centre for Dependency Care and Autonomous Living
Universitat Politècnica de Catalunya (BarcelonaTech). Vilanova i la Geltrú (08800), Spain
activityrecognition '@' smartlab.ws 
Retrieved from https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Dataset Analysis:
The code run_analysis.R performs the five steps explained in the course project's introduction.
- First step, all the related data is merged using the rbind() function. By related, we look into those files having the same number of columns and referring to the same entities. 
- Next, only those columns with the mean and standard deviation measures are picked from the whole dataset. 
After extracting these columns, they are given the correct names, taken from features.txt. 
-An activity data is addressed with values 1:6, the activity names and IDs from activity_labels.txt are taken and they 
are substituted in the dataset. 
-	In the entire dataset, those columns with unclear column names are corrected. 
-	Lastly, we generate a new dataset with all the average measures for each subject and activity type 
(30 subjects * 6 activities = 180 rows). The output file is called averages_data.txt, and uploaded to this repository. 

Dataset Variables:
-	x_train, y_train, x_test, y_test, subject_train and subject_test have the data from the downloaded files. 
-	x_data, y_data and subject_data merge the previous datasets for further analysis. 
-	Features contains the right names for the x_data dataset, which are applied to the column names stored in 
mean_and_std_features, a numeric vector used to extract the desired data. 
-	A similar approach is taken with activity names through the activities variable. 
- All_data merges x_data, y_data and subject_data in a big dataset. 
-	Lastlly, averages_data contains the relevant averages which will be later stored in a .txt file. ddply(), 
plyr package is used to apply colMeans() and to make analysis easier.
