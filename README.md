Getting and Cleaning Data: Course Project
=========================================

Introduction
------------
This repository contains my solution to the course project for the Coursera course "Getting and Cleaning data", the 3rd part of the Data Science specialization.

About how the `run_analysis.R` script works
-----------------------------------------
- unzip the data from [wearable computing dataset](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) and rename the folder with "data".
- make sure the folder "data" and the `run_analysis.R` script are both in the current working directory.
- run `run_analysis.R` in RStudio.
- the script generates two tab-delimited files in the current working directory:
	- `merged_data.txt` (contains a data frame called cleanedData)
	- `data_with_means.txt` (a tidy data set containing the means of all the columns per subject and per activity)
- use `data <- read.table("data_with_means.txt")` command in RStudio to read the file

About the Code Book
-------------------
The `CodeBook.md` file explains all the variables and summaries calculated, along with units, and any other relevant information.

