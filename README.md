# Getting-and-Cleaning-Data-Course-Project

The purpose of this project was to demonstrate the ability to collect, work with, and clean a data set. The goal was to prepare tidy data that can be used for later analysis.  As well as this README file, there is an R script in this repo called **run_analysis.R** and also a markdown file called **CodeBook.md**

The  **run_analysis.R** does the following:

1.	Merges the training and the test sets to create one data set.
2.	Extracts only the measurements on the mean and standard deviation for each measurement. 
3.	Uses descriptive activity names to name the activities in the data set
4.	Appropriately labels the data set with descriptive variable names. 
5.	From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


the file **run_analysis.R** is annotated and gives details of how each step was performed in R. 

The **CodeBook** markdown file in this repo gives some background details and details of the variables and some explanatory notes.  Both of these should be looked at in conjunction with this README file as the intention is not to repeat information that is in each of the two other files.

A few key points to make about the exercise:

######"Extracts only the measurements on the mean and standard deviation for each measurement"######

+ This was done by examining the accelerometer data for the terms *mean()* and *sd()*.  Reviewing the variables in the   *features_info.txt* file that came with the data, it was decided that the *meanFreq* variables should also be         dropped. This reduced the total number of (accelerometer) variables from 559 to 73.  

######"Uses descriptive activity names to name the activities in the data set"######
######"Appropriately labels the data set with descriptive variable names"######

+ The activity labels and the variable names were read in from the files that came with the data - *actvity_labels.txt* and *features.txt*.  In addition the subject identifier data was in *subject_train.txt* and *subject_test.txt*.

+ These were combined with the other data to get the full data set of 10,299 observations of 75 variables (including *subject* and *activity* variables) with descriptive activity names and appropriate descriptive variable names.

######"From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject."######

+ The *aggregate* function was used to derive the tidy data set, with the average of each of the 73 accelerometer variables for each activity for each subject.  This gave a data set with a total of 180 observations on 75 variables.  This was the average of each variable for the 30 subjects for each of the 6 activities

+ This data was written to a text file **tidySamsungdata.txt"* using *write.table* with *row.names=FALSE* and attached as a text file to the coursework site

+ If this data is examined as a text file it looks alittle messy. As stated in the R script it is better to run the following which clealry shows the tidy format of the data:
 
+ data <- read.table("tidySamsungdata.txt", header = TRUE); View(data)
[I would like to acknowledge the following thread from the following discussion thread for this idea: 
https://class.coursera.org/getdata-011/forum/thread?thread_id=69]






