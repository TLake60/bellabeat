# Description
This repository contains two files for the capstone project I completed for the Google Data Analytic Certification on Coursera.  
* The Power BI report containing the data model and visualizations I created to explore and analyze the Kaggle dataset for the capstone project 
* The PowerPoint presentation developed in response to the business challenge

The actual Kaggle project containing the R code used to read, transform, analyze, and present the data and my findings can be found at https://www.kaggle.com/code/terencelake/bellabeat-googlecapstone-r-powerbi
# Capstone Project
The Google Analytics capstone project I chose was the Bellabeat case study. 
The business task was to analyze non-Bellabeat smart device usage (using public FitBit data) to gain insights into consumer usage trends.  These insights were to be used to make high-level, marketing strategy recommendations to the Bellabeat Executive Team focused on growing the revenue of one of Bellabeat’s smart device products.  
# Data Source
Fitbit Fitness Tracker Data dataset of 18 csv files from Kaggle.  It is a public domain dataset made available through Mobius.
The files represent the activity of 33 Fitbit users over a one-month period from 4/12/16 to 5/12/16 and track daily activity by minute, hour, and day in a long format and additionally in wide format for a select number of files.
Generally, the metrics tracked are:
* Weight
* Sleep time
* Calories burned
* Steps taken and distance travelled
# Process
I initially used Power BI extract and explore the data.
## Power BI Desktop Steps
### Step 1
1.	Inspected the summarized daily activities table
a.	Not every user has data for all 31 days
i.	Must categorize in user levels 
2.	Loaded all the other files into Power BI Desktop
3.	Saved as FitBit Model.pbix
4.	Changed data type of all ID columns to text so as not to accidentally person any calculations on them
### Step 2
1.	Created a User ID table to use IDs as primary key to create summary tables aggregating data from each table.  The ID will also be used to show the relationships between tables.
2.	Queried daily activity table to highlight number of days each Fitbit User wore device during the study period based on the number of days of activity provided.  This was used to categorize user levels.  This same concept will be used to investigate use during sleep, % of day device is worn, day of week, and whether it is used to monitor health statistics and modify behavior.  
3.	Renamed all the data model table to remove the _merged suffix.
4.	Revised the Fitbit csv file and added it to the data model to use as the primary key fact table 
5.	Connected all fact tables to the User ID table by their ID columns.
### Step 3
1.	Created a Use Date calculated table.
2.	Added User Month, User Day, and Weekend_day columns to the table.
3.	Related the date table to all fact tables in the model by their date or date/time columns.
### Step 4
1.	Formatted numeric columns in all data model tables - formatted whole number columns to have commas and all others to be 2-digit, decimal numbers.
2.	Corrected to text fields, all ID columns that weren’t designated as such.
3.	Have a credible data model with which to conduct analysis.

When I realized that I needed the cloud version of Power BI to export the files into PowerPoint I exported the data from some of the visualization into excel power pivot and recreated the charts.  This is the PowerPoint file included in this repository.
I then recreated the process in R and copied, pasted, and adapted a streamlined version in Kaggle as the final project.
