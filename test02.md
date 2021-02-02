R Markdown
----------

### Introduction

The requirement is as follows:  
- Merges the training and the test sets to create one data set.  
- Extracts only the measurements on the mean and standard deviation for
each measurement.  
- Uses descriptive activity names to name the activities in the data
set.  
- Appropriately labels the data set with descriptive variable names.  
- The data set in step 4, creates a second, independent tidy data set
with the average of each variable for each activity and each subject.

### Methods:

1.  Downloading of Dataset and extract into folder “Data”.

2.  Merge the test and training data.  
    `x_train`: training set (7352 obs. of 561 variables)  
    `y_train`: training lables (7352 obs. of 1 variable)  
    `subject_train` - Each row identifies subject who performed activity
    for each window sample.  
    `x_test` - test set.  
    `y_test` - test labels  
    `subject_test` - Each row identifies subject who performed activity
    for each window sample.  
    `X_data` - combine x\_train, x\_test using rows  
    `Y_data` - combine y\_train, y\_test using rows  
    `Subject_data` - combine subject\_train, subject\_test using rows  
    Extract the following  
    feature - list of features  
    activity\_label - list of activities  
    myColumns - list of columns containing “mean” or “Std”(standard
    deviation)

3.  Extracts only the measurements on the mean and standard deviation
    for each measurement.  
    X\_data - extract only the data with “my columns” (containing “mean”
    or “Std”(standard deviation))

4.  Uses descriptive activity names to name the activities in the data
    set; Appropriately labels the data set with descriptive variable
    names.  
    Merges training and test sets to create one data set MergedData  

-   Combine X, Y, Subject using selected columns  
-   append the activity column  
-   append the subject column

1.  From the data set in step 4, creates a second, independent tidy data
    set with the average of each variable for each activity and each
    subject  
    myTidyData:  

-   Use the MergedData above  
-   Based on the Activity, and subject combination (as “variant”) to
    calculate the average value
-   Export myTidyData into myTidyData.txt file
