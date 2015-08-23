## Project Description
This is the Course Project for the "Getting and Cleaning Data" course.
We are requested to take the wearable data from Samsung Galaxy S II and tidy it up. 

##Study design and data processing

###Collection of the raw data
The data was downloaded from the link: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
Here is a full description of the data: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

###Notes on the original (raw) data 
The original data was divided in 6 .txt files which were separated in 3 groups:
1: A vector of codes for each subject.
2: A vector of codes for each action recorded.
3: A matrix of the collected data.

##Creating the tidy datafile

###Guide to create the tidy data file
The data was created by downloading the raw data form the link above;
Opening each file in R;
Modifying the data so that they can all be merged together;
Merging and labeling the data acordingly;
Taking the mean of each variable by action and subject.

###Cleaning of the data
The details of how the data was cleaned is at the following link:


##Description of the variables in the tiny_data.txt file
The dataset has 180 observations of 69 variables.
The data are a summary of the raw data taken the mean by subject and action.
A general summary of the data is as follows:
 set                      : Factor w/ 2 levels "test","train": 1 1 1 1 1 1 1 1 1 1 ...
 subject                  : int  2 2 2 2 2 2 4 4 4 4 ...
 action                   : Factor w/ 6 levels "WALKING","WALKING_UPSTAIRS",..: 1 2 3 4 5 6 1 2 3 4 ...
 tBodyAcc-mean-X          : num  0.276 0.247 0.278 0.277 0.278 ...
 tBodyAcc-mean-Y          : num  -0.0186 -0.0214 -0.0227 -0.0157 -0.0184 ...
 tBodyAcc-mean-Z          : num  -0.106 -0.153 -0.117 -0.109 -0.106 ...
 tBodyAcc-std-X           : num  -0.4236 -0.3044 0.0464 -0.9868 -0.9873 ...
 tBodyAcc-std-Y           : num  -0.0781 0.108 0.2629 -0.9507 -0.9573 ...
 tBodyAcc-std-Z           : num  -0.425 -0.112 -0.103 -0.96 -0.95 ...
 tGravityAcc-mean-X       : num  0.913 0.791 0.862 0.94 0.897 ...
 tGravityAcc-mean-Y       : num  -0.347 -0.416 -0.326 -0.106 -0.37 ...
 tGravityAcc-mean-Z       : num  0.0847 -0.1959 -0.0439 0.1987 0.1297 ...
 tGravityAcc-std-X        : num  -0.973 -0.934 -0.94 -0.98 -0.987 ...
 tGravityAcc-std-Y        : num  -0.972 -0.924 -0.94 -0.957 -0.974 ...
 tGravityAcc-std-Z        : num  -0.972 -0.878 -0.931 -0.954 -0.946 ...
 tBodyAccJerk-mean-X      : num  0.0618 0.0745 0.11 0.0723 0.0748 ...
 tBodyAccJerk-mean-Y      : num  0.01825 -0.00971 -0.00328 0.0117 0.01033 ...
 tBodyAccJerk-mean-Z      : num  0.0079 0.01948 -0.02094 0.00761 -0.00837 ...
 tBodyAccJerk-std-X       : num  -0.278 -0.276 0.147 -0.988 -0.981 ...
 tBodyAccJerk-std-Y       : num  -0.0166 -0.1856 0.1268 -0.978 -0.9711 ...
 tBodyAccJerk-std-Z       : num  -0.586 -0.574 -0.34 -0.988 -0.983 ...
 tBodyGyro-mean-X         : num  -0.053 -0.0577 -0.1159 -0.0455 -0.0239 ...
 tBodyGyro-mean-Y         : num  -0.04824 -0.03209 -0.00482 -0.05993 -0.08204 ...
 tBodyGyro-mean-Z         : num  0.0828 0.0688 0.0972 0.0412 0.0878 ...
 tBodyGyro-std-X          : num  -0.562 -0.439 -0.321 -0.986 -0.973 ...
 tBodyGyro-std-Y          : num  -0.538 -0.466 -0.416 -0.979 -0.971 ...
 tBodyGyro-std-Z          : num  -0.481 -0.164 -0.279 -0.96 -0.965 ...
 tBodyGyroJerk-mean-X     : num  -0.0819 -0.0829 -0.0581 -0.0936 -0.1056 ...
 tBodyGyroJerk-mean-Y     : num  -0.0538 -0.0424 -0.0421 -0.0416 -0.0422 ...
 tBodyGyroJerk-mean-Z     : num  -0.0515 -0.0445 -0.071 -0.0436 -0.0547 ...
 tBodyGyroJerk-std-X      : num  -0.39 -0.465 -0.244 -0.99 -0.979 ...
 tBodyGyroJerk-std-Y      : num  -0.634 -0.645 -0.469 -0.991 -0.983 ...
 tBodyGyroJerk-std-Z      : num  -0.435 -0.468 -0.218 -0.986 -0.974 ...
 tBodyAccMag-mean         : num  -0.29 -0.107 0.09 -0.968 -0.966 ...
 tBodyAccMag-std          : num  -0.423 -0.206 0.216 -0.953 -0.958 ...
 tGravityAccMag-mean      : num  -0.29 -0.107 0.09 -0.968 -0.966 ...
 tGravityAccMag-std       : num  -0.423 -0.206 0.216 -0.953 -0.958 ...
 tBodyAccJerkMag-mean     : num  -0.28142 -0.32127 0.00566 -0.98677 -0.98049 ...
 tBodyAccJerkMag-std      : num  -0.164 -0.217 0.23 -0.984 -0.977 ...
 tBodyGyroMag-mean        : num  -0.447 -0.22 -0.162 -0.946 -0.963 ...
 tBodyGyroMag-std         : num  -0.553 -0.378 -0.275 -0.961 -0.954 ...
 tBodyGyroJerkMag-mean    : num  -0.548 -0.573 -0.411 -0.991 -0.984 ...
 tBodyGyroJerkMag-std     : num  -0.558 -0.597 -0.343 -0.99 -0.977 ...
 fBodyAcc-mean-X          : num  -0.346 -0.267 0.113 -0.986 -0.984 ...
 fBodyAcc-mean-Y          : num  -0.0219 0.00992 0.27835 -0.95734 -0.95987 ...
 fBodyAcc-mean-Z          : num  -0.454 -0.281 -0.131 -0.97 -0.962 ...
 fBodyAcc-std-X           : num  -0.4577 -0.3206 0.0161 -0.9874 -0.9891 ...
 fBodyAcc-std-Y           : num  -0.1692 0.0849 0.172 -0.9501 -0.9579 ...
 fBodyAcc-std-Z           : num  -0.4552 -0.0945 -0.162 -0.9569 -0.9464 ...
 fBodyAccJerk-mean-X      : num  -0.305 -0.259 0.138 -0.988 -0.981 ...
 fBodyAccJerk-mean-Y      : num  -0.0788 -0.1878 0.0962 -0.9771 -0.9709 ...
 fBodyAccJerk-mean-Z      : num  -0.555 -0.523 -0.271 -0.985 -0.98 ...
 fBodyAccJerk-std-X       : num  -0.314 -0.365 0.05 -0.989 -0.983 ...
 fBodyAccJerk-std-Y       : num  -0.0153 -0.2436 0.0808 -0.9808 -0.9735 ...
 fBodyAccJerk-std-Z       : num  -0.616 -0.625 -0.408 -0.989 -0.985 ...
 fBodyGyro-mean-X         : num  -0.43 -0.332 -0.146 -0.983 -0.967 ...
 fBodyGyro-mean-Y         : num  -0.555 -0.488 -0.362 -0.982 -0.973 ...
 fBodyGyro-mean-Z         : num  -0.3967 -0.2486 -0.0875 -0.9598 -0.9606 ...
 fBodyGyro-std-X          : num  -0.604 -0.476 -0.379 -0.987 -0.975 ...
 fBodyGyro-std-Y          : num  -0.533 -0.46 -0.459 -0.977 -0.971 ...
 fBodyGyro-std-Z          : num  -0.56 -0.218 -0.423 -0.964 -0.97 ...
 fBodyAccMag-mean         : num  -0.324 -0.145 0.293 -0.961 -0.964 ...
 fBodyAccMag-std          : num  -0.5771 -0.3667 -0.0215 -0.9556 -0.9605 ...
 fBodyBodyAccJerkMag-mean : num  -0.169 -0.19 0.222 -0.984 -0.977 ...
 fBodyBodyAccJerkMag-std  : num  -0.164 -0.26 0.227 -0.984 -0.975 ...
 fBodyBodyGyroMag-mean    : num  -0.531 -0.451 -0.321 -0.972 -0.962 ...
 fBodyBodyGyroMag-std     : num  -0.652 -0.439 -0.373 -0.961 -0.957 ...
 fBodyBodyGyroJerkMag-mean: num  -0.583 -0.601 -0.38 -0.99 -0.978 ...
 fBodyBodyGyroJerkMag-std : num  -0.558 -0.622 -0.344 -0.99 -0.978 ...
 
 
### set
This variable describes which set of recordings this observation comes from, the "test" set or the "train" set.

 - Factor variable
 - 1 == test
 - 2 == train
 - no unit of measurement.

### subject
This variable describes which subject this observation was recorded from.

 - Factor variable
 - 30 levels, one for each subject.
 - no unit of measurement.

### action
This variable describes which action was being performed by the subject during this recording.

 - Factor variable
 - 6 levels.
 -- 1 == WALKING
 -- 2 == WALKING_UPSTAIRS
 -- 3 == WALKING_DOWNSTAIRS
 -- 4 == SITTING
 -- 5 == STANDING
 -- 6 == LAYING
 - no unit of measurement.

### tBodyAcc-mean-X
Mean of the body acceleration signal on the X axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAcc-mean-Y
Mean of the body acceleration signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAcc-mean-Z
Mean of the body acceleration signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAcc-std-X
Standard deviation of the body acceleration signal on the X axis 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAcc-std-Y
Standard deviation of the body acceleration signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAcc-std-Z
Standard deviation of the body acceleration signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-mean-X
Mean of the gravity acceleration signal on the X axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-mean-Y
Mean of the gravity acceleration signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-mean-Z
Mean of the gravity acceleration signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-std-X
Standard deviation of the gravity acceleration signal on the X axis 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-std-Y
Standard deviation of the gravity acceleration signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAcc-std-Z
Standard deviation of the gravity acceleration signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-mean-X
Mean of the body acceleration jerk (linear and angular) signal on the X axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-mean-Y
Mean of the body acceleration jerk (linear and angular) signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-mean-Z
Mean of the body acceleration jerk (linear and angular) signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-std-X
Standard deviation of the body acceleration jerk (linear and angular) signal on the X axis 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-std-Y
Standard deviation of the body acceleration jerk (linear and angular) signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerk-std-Z
Standard deviation of the body acceleration jerk (linear and angular) signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-mean-X
Mean of the body gyroscope signal on the X axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-mean-Y
Mean of the body gyroscope signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-mean-Z
Mean of the body gyroscope signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-std-X
Standard deviation of the body gyroscope signal on the X axis 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-std-Y
Standard deviation of the body gyroscope signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyro-std-Z
Standard deviation of the body gyroscope signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-mean-X
Mean of the body gyroscope jerk (linear and angular) signal on the X axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-mean-Y
Mean of the body gyroscope jerk (linear and angular) signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-mean-Z
Mean of the body gyroscope jerk (linear and angular) signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-std-X
Standard deviation of the body gyroscope jerk (linear and angular) signal on the X axis 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-std-Y
Standard deviation of the body gyroscope jerk (linear and angular) signal on the Y axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerk-std-Z
Standard deviation of the body gyroscope jerk (linear and angular) signal on the Z axis
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccMag-mean
Mean of the boddy acceleration signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccMag-std
Standard deviation of the boddy acceleration signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAccMag-mean
Mean of the gravity acceleration signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tGravityAccMag-std
Standard deviation of the gravity acceleration signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerkMag-mean
Mean of the body acceleration jerk (linear and angular) signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyAccJerkMag-std
Standard deviation of the body acceleration jerk (linear and angular) signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroMag-mean
Mean of the body gyroscope signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroMag-std
Standard deviation of the body gyroscope signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerkMag-mean
Mean of the body gyroscope jerk (linear and angular) signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### tBodyGyroJerkMag-std
Standard deviation of the body gyroscope jerk (linear and angular) signal magnitude using the Euclidean norm.
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-mean-X
Fast Fourier Transform (FFT) applied to tBodyAcc-mean-X 
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-mean-Y
Fast Fourier Transform (FFT) applied to tBodyAcc-mean-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-mean-Z
Fast Fourier Transform (FFT) applied to tBodyAcc-mean-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-std-X
Fast Fourier Transform (FFT) applied to tBodyAcc-std-X
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-std-Y
Fast Fourier Transform (FFT) applied to tBodyAcc-std-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAcc-std-Z
Fast Fourier Transform (FFT) applied to tBodyAcc-std-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-mean-X
Fast Fourier Transform (FFT) applied to tBodyAccJerk-mean-X
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-mean-Y
Fast Fourier Transform (FFT) applied to tBodyAccJerk-mean-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-mean-Z
Fast Fourier Transform (FFT) applied to tBodyAccJerk-mean-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-std-X
Fast Fourier Transform (FFT) applied to tBodyAccJerk-std-X
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-std-Y
Fast Fourier Transform (FFT) applied to tBodyAccJerk-std-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccJerk-std-Z
Fast Fourier Transform (FFT) applied to tBodyAccJerk-std-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-mean-X
Fast Fourier Transform (FFT) applied to tBodyGyro-mean-X
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-mean-Y
Fast Fourier Transform (FFT) applied to tBodyGyro-mean-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-mean-Z
Fast Fourier Transform (FFT) applied to tBodyGyro-mean-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-std-X
Fast Fourier Transform (FFT) applied to tBodyGyro-std-X
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-std-Y
Fast Fourier Transform (FFT) applied to tBodyGyro-std-Y
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyGyro-std-Z
Fast Fourier Transform (FFT) applied to tBodyGyro-std-Z
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccMag-mean
Fast Fourier Transform (FFT) applied to tBodyAccMag-mean
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyAccMag-std
Fast Fourier Transform (FFT) applied to tBodyAccMag-std
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyAccJerkMag-mean
Fast Fourier Transform (FFT) applied to tBodyBodyAccJerkMag-mean
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyAccJerkMag-std
Fast Fourier Transform (FFT) applied to tBodyBodyAccJerkMag-std
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyGyroMag-mean
Fast Fourier Transform (FFT) applied to tBodyBodyGyroMag-mean
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyGyroMag-std
Fast Fourier Transform (FFT) applied to tBodyBodyGyroMag-std
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyGyroJerkMag-mean
Fast Fourier Transform (FFT) applied to tBodyBodyGyroJerkMag-mean
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

### fBodyBodyGyroJerkMag-std
Fast Fourier Transform (FFT) applied to tBodyBodyGyroJerkMag-std
Variable is unitless because it was normalised.
Variable can assume values between -1 and 1.

##Sources
Coursera Getting and Cleaning Data
