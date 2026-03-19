# predicting-legal-outcomes-Wichita-traffic-stops
The project will explored traffic citations and dispositions from those citations using data from the Stanford Open Policing Project for Wichita, Kansas. The core question we aim to answer is: does subject demographic information (race, sex and/or age) have an effect on the severity of dispositions resulting from a citation. 

# Team: Dr Alex Bevan, Akshaya Ganesh, Ryan Abdelrahim

# Objective:
The objective is to provide a clear, data-driven solution to the question posed above.

# Data Description:
The dataset comes from the Stanford Open Policing Project (OPP), which has compiled over 200 million traffic stop records from across the United States. The dataset for Wichita, KS contains 1 million records from 2006 through 2020 (2017 excluded) along with 22 variables. Variables from the dataset were used to derive more informational predictors listed here:

year, month, day_of_week, hour - obtained from the original 'date’ and ‘time’ variables in the dataset. Decomposition was performed in hopes that a pattern may arise regarding an increase in citations (winter vs summer, night time vs day time, weekend vs weekday etc)
violation_severity - obtained from binning the original ‘violation’ variable by key words and ranking severity as 1, 2 or 3 (for low , medium and high severity respectively)
subject_race, subject_sex, age_category - ‘subject_race’ and ‘subject_sex’ were taken as is from the dataset while ‘age_category’ was created from binning ‘subject_age’
city_location - was created by extracting zipcodes from ‘location’ and binning them by which side of the city they fall in
‘vehicle_teir’ - ‘vehicle_make’ was binned into categories for pedestrian vehicles by worth (budget, legacy, luxury and mid) and all other vehicles were binned as either motorcycle, trailer or unknown
‘disposition_severity’ - obtained from binning the original ‘disposition’ variable by key words and ranking severity as 0, 1, 2 or 3 (for unknown, low, medium and high severity respectively)

# Model
While the project was joint, I made my own individual Logistic Regression model achieved a 11.6 Rsquared score which is in keeping with the domain standards of criminology and human subject research
