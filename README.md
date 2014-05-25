There are 4 parts in the code to get the new tidy data set as requested.

Part1: The codes in this part was used to load the training and test datasets into R. I created a character vector in this part for all the feature names by using 'features.txt'.  I append the subjects and activity to the training/test dataset in this step. In order to separate the training and test data, I created a new variable called  ‘group’ with two levels - ‘training’ and ‘test’.


Part2: The codes in this part was used to do data manipulation. Training and test datasets were merged firstly to be one large table. I also check the sample size, roughly 70% for training and 30% for test, consistent with the README file for the data. ‘grep’ function was used here to extracts only the measurements on the mean and standard deviation for each measurement. ‘meanFreq’ was ignore here, only future names with ‘mean()’ and ‘std()’ were kept.

Part3: The codes in this part was used to use descriptive activity names to name the activities in the data set. Inner join was applied here to append descriptive activity names to dataset by using the lookup table ‘activity_labels.txt’.

Part4: The codes in this part was used to create a second, independent tidy data set with the average of each variable for each activity and each subject. The average value for all the columns ONLY based on activity and subject. So training and test data were mixed here. I renamed all the columns that were averaged and added “mean” at the end of their names. The final output is a .txt file with subject, activity name and the average value of each variable for each activity and each subject.