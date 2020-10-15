# Getting-and-Cleaning-Data-Course-Project
The following text describes stage by staage the procedure to create the desired tidy data: 

## 1. Preparation stage:
### Loading packages
The main package in this script is dplyr
### Directory
With the functions of getwd() and setwd(), the directory is set, accordingly with the folder organization
### Download data
The UCI HAR Dataset is downloadem from the supplied URL with the functions file.exists, download.file and unzip.
### Import all data to the environment
All .txt files are imported with the read.table function. 

## 2. Merging Stagesubject_test data.
With rbind the x and y train and tests datasets are merged. The same is done with subject_train and subject_test data.
Finally, with cbind we get the merged_data form subject, Y and X.  

## 3. Mean and standard deviation from data
Mean and sd is calculated with select. 

## 4. Descriptive activity names
With [] descriptive activity names are set. 

## 5. Appropiate labels
With gsub the appropiate labels are set. 

## 6. Final Dataset
The final Dataset is created with the following function group_by, >%>, summarise.all and write.table. 
