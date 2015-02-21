#   Code Book for Tidy Data Set "tidySamsungdata"
##  Please also see README in this repo

These data were derived from experiments that have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, data were captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. The acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ). Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag.  
These signals were used to estimate variables of the feature vector for each pattern: '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

There were several variables estimated from these signals (see the README.txt file associated with the Samsung accelerometer data) but for the purpose of this course project only variables that had mean (mean()) or std (std()) values were retained. This was done by examining the accelerometer variables and their definitions for the terms mean() and sd(). Reviewing the variables in the features_info.txt file that came with the data, it was decided that the meanFreq variables should also be dropped. This reduced the total number of (accelerometer) variables from 561 to 73. MeanFreq variables were also dropped. This meant we kept 75 of the original 561 variables (including subject and activity).  Each of these variables are normalized and bounded within [-1,1].

The activity labels and the variable names were read in from the files that came with the data - *actvity_labels.txt* and *features.txt*.  In addition the subject identifier data was in *subject_train.txt* and *subject_test.txt*.  These were combined with the other data to get the full data set of 10,299 observations of 75 variables (including *subject* and *activity* variables) with descriptive activity names and appropriate descriptive variable names.

To produce the final data set, we derived the mean of each variable for each subject performing each of the six activities and only retained these mean values. Therefore the final data set had 75 variables (73 of these were the average of each of the relevant accelerometer measurements) together with subject and activity, and 180 observations (30 subject measured on each of 6 activities).  Below is a brief summary of each of the variables

##  Variables and Descriptions

####subject

30 volunteers numbered 1-30

####activity

The six activities carried out by each subject. These are WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, and LAYING

####tBodyAcc-mean()-X
####tBodyAcc-mean()-Y
####tBodyAcc-mean()-Z
####tBodyAcc-std()-X
####tBodyAcc-std()-Y
####tBodyAcc-std()-Z
####tGravityAcc-mean()-X
####tGravityAcc-mean()-Y
####tGravityAcc-mean()-Z
####tGravityAcc-std()-X
####tGravityAcc-std()-Y
####tGravityAcc-std()-Z
####tBodyAccJerk-mean()-X
####tBodyAccJerk-mean()-Y
####tBodyAccJerk-mean()-Z
####tBodyAccJerk-std()-X
####tBodyAccJerk-std()-Y
####tBodyAccJerk-std()-Z
####tBodyGyro-mean()-X                  
####tBodyGyro-mean()-Y
####tBodyGyro-mean()-Z
####tBodyGyro-std()-X
####tBodyGyro-std()-Y
####tBodyGyro-std()-Z
####tBodyGyroJerk-mean()-X              
####tBodyGyroJerk-mean()-Y
####tBodyGyroJerk-mean()-Z
####tBodyGyroJerk-std()-X               
####tBodyGyroJerk-std()-Y
####tBodyGyroJerk-std()-Z
####tBodyAccMag-mean()                  
####tBodyAccMag-std()
####tGravityAccMag-mean()
####tGravityAccMag-std()                
####tBodyAccJerkMag-mean()
####tBodyAccJerkMag-std()
####tBodyGyroMag-mean()
####tBodyGyroMag-std()
####tBodyGyroJerkMag-mean()
####tBodyGyroJerkMag-std()
####fBodyAcc-mean()-X
####fBodyAcc-mean()-Y
####fBodyAcc-mean()-Z
####fBodyAcc-std()-X
####fBodyAcc-std()-Y
####fBodyAcc-std()-Z
####fBodyAccJerk-mean()-X
####fBodyAccJerk-mean()-Y
####fBodyAccJerk-mean()-Z
####fBodyAccJerk-std()-X
####fBodyAccJerk-std()-Y
####fBodyAccJerk-std()-Z
####fBodyGyro-mean()-X
####fBodyGyro-mean()-Y
####fBodyGyro-mean()-Z                  
####fBodyGyro-std()-X
####fBodyGyro-std()-Y
####fBodyGyro-std()-Z                   
####fBodyAccMag-mean()
####fBodyAccMag-std()
####fBodyBodyAccJerkMag-mean()          
####fBodyBodyAccJerkMag-std()
####fBodyBodyGyroMag-mean()
####fBodyBodyGyroMag-std()              
####fBodyBodyGyroJerkMag-mean()
####fBodyBodyGyroJerkMag-std()
####angle(tBodyAccMean,gravity)         
####angle(tBodyAccJerkMean),gravityMean)
####angle(tBodyGyroMean,gravityMean)
####angle(tBodyGyroJerkMean,gravityMean)
####angle(X,gravityMean)
####angle(Y,gravityMean)
####angle(Z,gravityMean) 

Means for each of the mean() and SD() accelerometer variables for each subject performing each of the 6 activities
