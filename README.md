# Data 512 Final Project
## Analysis of Diversity in Outdoor Recreation in Washington
This repository contains the work for my final project for the Univeristy of Washington's DATA 512 Human Centered Data Science course, completed in Autumn 2018. This Readme gives an overview of the project, the repository structure, and the results. For more information on all parts of the project, please refer to the full project report in the wa_outdoor_recreation_analysis.ipynb file.

Please also note that everything in this repository is under the MIT license (https://opensource.org/licenses/MIT) unless otherwise noted.

## Introduction
Outdoor recreation is having a moment in the US. Having recently been valued by the Federal Government at $373 billion, with growth of 3.8% in 2016 alone, the outdoor industry is now officially a big deal. And yet, outdoor recreation has historically been defined by a complete lack of diversity, and the industry arguably won't reach its true potential until we make it more inclusive and representative of everybody. While this is problem is well known qualitatively, there is currently a lack of quantitative evidence on the specifics of the problem, which makes it difficult to accurately design and target programs meantw to diversify the outdoors.

This is what lead me to want to complete this analysis of diveristy in outdoor recreation in Washington. I focused on backcountry sports in particular, and set out to determine whether there was a statstically significant difference between participation rates among men and other genders, and those who identify as white and other races. I also created some visualizations of the data set. Overall, this human centered data science project was quite interesting, and hopefully the conclusions can help inform furture work as well as programs and targeted outreach designed to increase diversity in the outdoors.

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
All data used for this project came from the results of the Washington State 2013 Statewide Comprehensive Outdoor Recreation Plan (SCORP) survey. All of the data is made publically available and accessible by the State of Washington through data.wa.gov and through Socrata's API. The data is in the public domain (no license or copywright applicable), and so can be replicated and analyzed here without limitation. The full data set is provided in seven different csv files, all of which can be found at the 'Data Source' link given below; each part will be titled something like 'WA RCO SCORP 2013 Dataset Part X of 7'. 

Some relevant links regarding the data are provided below:

 - Data source: https://data.wa.gov/browse?category=Recreation
 - Socrata API: https://dev.socrata.com/
 - Socrata terms of service: https://socrata.com/terms-of-service/
 - Public Domain definition: https://en.wikipedia.org/wiki/Public_domain

## Analysis
My analysis for this project consisted of:

 1. Visualizing the distribution of survey respondents by gender and race
 2. Visualizing the proportion of respondents who participate in any backcountry sports, broken down by gender and race
 3. Visualizing the proportion of respondents who participate in specific backcountry sports, broken down by gender and race
 4. Hypothesis testing for population proportions to identify if there is a statistically significant difference in participation rates between the different genders or different races
 5. Calculation of 95% confidence intervals for the difference in population proportions for any of the statistically significant results from 4).

## Selected Results
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
I'd like to extend thanks to the University of Washington DATA 512 course instructors, Jonathan Morgan and Os Keyes, for providing guidance throughout this project and throughout the course. More information on the course can be found here: https://wiki.communitydata.cc/Human_Centered_Data_Science_(Fall_2018)

For more information about this project, please contact Kenten Danas at kentdanas@gmail.com
