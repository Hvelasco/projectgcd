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
General description of the file including:
 - Dimensions of the dataset
 - Summary of the data
 - Variables present in the dataset

(you can easily use Rcode for this, just load the dataset and provide the information directly form the tidy data file)

###Variable 1 (repeat this section for all variables in the dataset)
Short description of what the variable describes.

Some information on the variable including:
 - Class of the variable
 - Unique values/levels of the variable
 - Unit of measurement (if no unit of measurement list this as well)
 - In case names follow some schema, describe how entries were constructed (for example time-body-gyroscope-z has 4 levels of descriptors. Describe these 4 levels). 

(you can easily use Rcode for this, just load the dataset and provide the information directly form the tidy data file)

####Notes on variable 1:
If available, some additional notes on the variable not covered elsewehere. If no notes are present leave this section out.

##Sources
Coursera Getting and Cleaning Data
