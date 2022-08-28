# Project: Investigate No-show Appointments Dataset

## by Betabasi Daniel

## Introduction
### Dataset Description
The dataset that was used in this project is called "No-show appointments" and its original source is on [Kaggle](https://www.kaggle.com/datasets/joniarroba/noshowappointments). This dataset contains information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patients are included in each row. The dataset column labelled, ‘ScheduledDay’ tells us on what day the patient sets up their appointment. The column labelled, ‘Neighborhood’ indicates the location of the hospital. The column labelled, ‘Scholarship’ indicates whether or not the patient is enrolled in the Brasilian welfare program called [Bolsa Família](https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia).
> **NB:** The dataset has an encoding in the last column labelled, ‘No-show’ that says ‘No’ if the patient showed up to their appointment, and ‘Yes’ if they did not show up.

## Question for Analysis
What factors are important for us to know in order to predict if a patient will show up for their scheduled appointment?

## Data Wrangling
The following are the preliminary wrangling and wrangling steps I carried on the data:
1. I imported the packages I intend to use in my analysis process. 
2. I loaded the data file to my jupyter notebook and viewed the first few rows of the dataset. 
3. I inspected the dataset for missing or errant values, dimension, datatypes of columns and other useful information.
5. I converted the datatype of the ScheduledDay and AppointmentDay columns from strings to datetime. 
6. I checked for outliers in the Age column and I dropped the single row with the outlier of negative value. 
7. I dropped rows with duplicate values in PatientId column to avoid conflicting issues of analyzing the same patients repeatedly. 
8. I dropped PatientId and the AppointmentId columns since they had no impact on our predictions before I started exploring the dataset for insights.

## Summary of Findings
The results of my analysis indicates the following:
1. The ages of patients that miss their appointments more fall between the age range of 0 and 40 years. This implies that the younger people miss their appointments more than the elderly ones.
2. Patients that did not receive SMS but showed up for their appointments is higher as compared to the ones that received SMS.
3. Patients with chronic diseases like Hypertension and Diabetes tend to show more for their appointments than those without such chronic diseases.
4. Patients suffering from alcohlism show less for their appointments than the ones not suffering from it.
5. Patients on scholarship miss their appointments more than patients that were not on scholarship.

## Limitations 
The limitations of the dataset are as follows:
1. Most of the feature variables in the dataset I chose are categorical and does not allow high level of statistical analysis.
2. The correlation between different features in the dataset are not strong since most features have categorical data.
3. The statistics used in the dataset is descriptive and not inferential, hence I can not create any hypotheses with the data.
