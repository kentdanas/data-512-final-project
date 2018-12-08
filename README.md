# Data 512 Final Project
## Analysis of Diversity in Outdoor Recreation in Washington
Kenten Danas, Univeristy of Washington DATA 512, Autumn 2018

## Background

## Project Organization
This repository contains a jupyter notebook with a full report for this project as well as all necessary code, seven raw .csv data files resulting from API calls, two .csv files containing processed data, four .png files showing the results of the data visualization, and a final project plan and presentation. The repository has the following structure:

```
data-512-final-project/
  |- data_clean/
     |- gender_data_clean.csv
     |- race_data_clean.csv
  |- data_raw/
     |- scorp_8zc8-9ad4.csv
     |- scorp_amq9-iaai.csv
     |- scorp_ek6m-rgb7.csv
     |- scorp_hzyw-na2k.csv
     |- scorp_q62a-ce6s.csv
     |- scorp_uwas-gd9z.csv
     |- scorp_v2c2-rkrp.csv
  |- doc/
     |- final_project_plan.md
     |- final_project_presentation.pdf
  |- results/
     |- gender_participiation_in_backcountry_specific.png
     |- participiation_in_backcountry_general.png
     |- race_participiation_in_backcountry_specific.png
     |- respondent_distribution.png
  |- .gitignore
  |- LICENSE
  |- README.md
  |- wa_outdoor_recreation_analysis.ipynb
```

## Data Source

## Analysis

## Results
Results from the data visualization portion of this analysis can be found in the results/ folder of this repository. Results from the two-sided hypothesis and chi-squared tests for differences between the population proportions are shown in the following table:

| Population 1 | Population 2 | p-value | 
|--------------|--------------|---------|
|Male|Female| 0.025|
|White|Asian| 0.353|
|White|Hispanic/Latino| 0.086|
|White|American Indian/AK Native| 0.400|
|White|Black| 0.015|
|White|Haw/Pacific Islander| 0.788|
|White|Other| 0.277|
|White|Two or More| 0.534|

A full discussion of these results and their implications can be found in the project report (wa_outdoor_recreation_analysis.ipynb).

## Acknowledgements
I'd like to extend thanks to the University of Washington DATA 512 course instructors, Jonathan Morgan and Os Keyes, for providing guidance throughout this project. More information on the course can be found here: https://wiki.communitydata.cc/Human_Centered_Data_Science_(Fall_2018)

For more information about this project, please contact Kenten Danas at kentdanas@gmail.com
