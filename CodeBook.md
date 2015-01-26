## Codebook

### Data Introduction:
The data are obtained here:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The detailed explanation of the experiments is:
"The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 
The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain."
Which can be found at http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones.

### Variable Overview
The variables contained in the original data set were collected from 30 volunteers ranging in age from 19-48. Each person performed the following six activities wearing a smartphone (Galaxy S II) on their waist:

1. **Walking**: coded as WALKING
2. **Walking Upstairs**: coded as WALKING_UPSTAIRS
3. **Walking Downstairs**: coded as WALKING_DOWNSTAIRS
4. **Sitting**: coded as SITTING
5. **Standing**: coded as STANDING
6. **Laying**: coded as LAYING

Using the smartphone's embedded accelerometer and gyroscope, the team captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments were video-recorded to label the data manually. The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers were selected for generating the training data, and 30% were used for the test data.

### File Overview:
The dataset includes the following files:

* **README.txt**: study information and license documentation 
* **features_info.txt**: Shows information about the variables used on the feature vector 
* **features.txt**: List of all features 
* **activity_labels**.txt: Links the class labels with their activity name 
* **train/X_train.txt**: Training set 
* **train/y_train.txt**: Training labels 
* **test/X_test.txt**: Test set 
* **test/y_test.txt**: Test labels 

Train data files are described below. Equivalent Test data files having same properties are included in the data set.

* **train/subject_train.txt**: Each row identifies the subject who performed the activity for each window sample; Its range is from 1 to 30
* **train/Inertial Signals/total_acc_x_train.txt**: The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'
* **train/Inertial Signals/total_acc_y_train.txt**: The acceleration signal from the smartphone accelerometer Y axis in standard gravity units 'g 
* **train/Inertial Signals/total_acc_z_train.txt**: The acceleration signal from the smartphone accelerometer Z axis in standard gravity units 'g
* **train/Inertial Signals/body_acc_x_train.txt**: The body acceleration signal obtained by subtracting the gravity from the total acceleration
* **train/Inertial Signals/body_gyro_x_train.txt**: The angular velocity vector measured by the gyroscope for each window sample; The units are radians/second

###The Transformations:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

I first merged the training and the test sets to create one data set. Then I extracted only the measurements on the mean and standard deviation for each measurement, which are the variables with labels: mean() or std().
I added the descriptive activity names column to this data set and labelled the descriptive activity names according to 'activity_labels.txt'. I added the subject column to this data set and calcaluted the average of each variable for each activity and each subject. I stored the means in a new tidy data set. Finally, I wrote this tidy data set to a text file.
