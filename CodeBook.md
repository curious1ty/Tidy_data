
This file described how to reproduce the results presented in this repository. The R code for the is all presented in the file [run_analysis.R](/run_analysis.R).

Data
-----------------
*Download the data from this link https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

*After extracting the content of the ZIP file to the working directory, set working directory to UCI HAR Dataset, then [run_analysis.R](/run_analysis.R) script can be executed.

Transformations
------------------
In this section the transformation which are applied to the data are described. The steps below correspond to the steps in the [run_analysis.R](/run_analysis.R) file

*Read in the data from files

*Assigin column names to the data imported above

*Create the train and  test set

*Combine training and test data to create a final data set

*Create a vector for the column names from the finalData, which 
will be used to select the desired mean & stddev columns

*Extract only the measurements on the mean and standard deviation for each measurement.

*Create a logicalVector that contains TRUE values for the ID, mean & stddev columns and FALSE for others

*Subset finalData table based on the logicalVector to keep only desired columns

*Merge the finalData set with the acitivityType table to include descriptive activity 	names

*Updating the colNames vector to include the new column names after merge

*Cleaning up the variable names

*Reassigning the new descriptive column names to the finalData set

*Create a second, independent tidy data set with the average of each variable for each activity and each subject. 

*Create a new table, finalDataNoActivityType without the activityType column

*Summarizing the finalDataNoActivityType table to include just the mean of each variable for each activity and each subject

*Merging the tidyData with activityType to include descriptive acitvity names

*Export the tidyData set 

