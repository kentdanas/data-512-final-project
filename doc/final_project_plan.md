# Final Project Plan – An Analysis of Gender & Racial Diversity in Outdoor Recreation

Kenten Danas, DATA 512, Autumn 2018

## Introduction
Outdoor recreation is having a moment in the US. In Feburary of 2018, the federal Bureau of Economic Analysis (BEA) released a report which estimated that the outdoor recreation economy is worth almost $374 billion dollars, making it nearly 2% of the entire US GDP in 2016 (1). The report also stated that this industry grew a whopping 3.8% in 2016 alone, putting it a full percentage point ahead of the rest of the US economy in terms of growth. This report, initiated when President Obama signed the Outdoor Recreation Jobs and Economic Impact Act, was the first from a federal agency to quantify the size of this industry, and has important implications on whether outdoor recreation is treated by government as a big player. Given that increased outdoor recreation has been proven to be exceptional for our physical and mental health, as well as closely tied to important topics like conservation, environmental protection, and public lands policy, this work is a huge and very exciting step forward that shows positive results.

On the other hand, while interest in outdoor recreation has never been greater and growth is expected to continue, there is still much work to be done to make the outdoors more accessible to a wider range of people. While specific statistics are hard to come by, there is great consensus that historically, participation in outdoor recreation has been dominated by people who identify as white males. This isn't difficult to beleive given the preponderance of white cis males as the "face of the outdoors" everywhere from gear models to magazine covers (2). But the industry is aware of this problem and (hopefully) trying to change; in order for the industry to really reach its true potential, we need to make the outdoors a more inclusive, accessible place for everybody.

In many areas, the first step to tackling this problem is to gain a more thorough (and quantitative) understanding of what is happening now. At the state level, local recreation departments are trying to plan for how to accomodate increased interest in outdoor recreation, and are collecting data that would allow for an analysis of current diversity. In Washington, this work falls under the Statewide Comprehensive Outdoor Recreation Plan (SCORP), which "serves as a management tool to help decision-makers and providers better understand and prioritize the acquisition, renovation, and development of recreational resources statewide for the next 5 years" (3). As part of SCORP, in 2013 Washington conducted a survey of more than 3,000 residents across the state about their participation in outdoor recreation. While the state did release a detailed report with findings from the survey (4), it lacked an in-depth analysis of the voluntary demographic information that was collected. For this project, I plan to use the results of the 2013 SCORP survey to take a deeper look at the gender and racial trends in participation in certain outdoor recreation activities, including a robust statistical analysis and visualization of results. Hopefully the results will shed some light on what is currently happening with minorities in outdoor recreation, and illuminate areas that are ripe for targeted work to get people more involved.

## Data
The data to be used for this project will be taken from .... All of the data is made publically available and accessible by the State of Washington.

#### Study Information

#### Data Source

#### Potential Data Limitations
There are several possible limitations with this data set as it relates to the analysis I plan to do (more on this below). One is that the survey was conducted in 2013, and so may not be representative of current outdoor recreation use, especially across minority demographics. The outdoor recreation industry has grown a substantial amount since 2013, and efforts to get more people involved in outdoor activities have been widely publisized. Ideally, for an analysis like this that attempts to quantify the extent of minority participation in outdoor activities, I would want more recent data. But for now, this data will serve as a benchmark.

Another potential limitation is that because all of the questions in the survey were voluntary, and the survey was quite lengthy, there may be many missing values. Missing data on participation in various activities may be easier to deal with depending on which activities I choose to focus the analysis on, but missing data on demographics like gender and race identification would require me to discard the entire observation for this analysis.

Finally, this data set has significant limitations for any gender analysis (see plan below) due to how gender information was collected. Rather than being asked as a question in which participants could self-identify, gender was determined by the interviewer presumably based on the participant's voice. Additionally, while this isn't discussed explicitly in the survey methodology, it appears based on the data that only binary options were used (the data contains only "male", "female" and "don't know"). This is problematic not only because it excludes transgender people entirely from the results, but also because it potentially misclassifies people's gender by basing the classification on a trait (voice) that is not necessarily an accurate predictor of the gender someone identifies with.


## Research Questions
At a high level, I plan to do a statistical analysis of diversity in participation in various outdoor recreational activities. 

#### Racial Diversity
My first research question will focus on how the results of the survey varied by self-identified race. Specifically, is there a statistically significant difference in the participation in various activities of white versus non-white respondents? And if non-white respondents were less likely to participate in certain activities, by how much? This will build off of SCORP's final report, which did some cursory analysis of diveristy based solely on the percent of white and non-white respondents who reportedly engaged in certain activities (3); there was no statistical analysis or visualization of the results in the report. Additionally, I will complete this analysis for each racial group included in the survey, as opposed to just white or non-white.

To do this analysis I plan to use a 2-sample Z-test. Note that I am assuming based on the number of survey respondents that my 'n' for each group will be sufficiently large even after cleaning the data; however, if it is not I can use a 2-sample t-test with a different test statistic. My null hypothesis will be that there is no difference in participation between white respondents and respondents of each other race. I will use a p-value of 0.05. For this analysis I will have to assume that the populations are normally distributed and that there are equal variances between each group; this may not actually be the case, but it should be an okay assumption for my purposes here (simply trying to get a ballpark sense of the differences).

I also plan to create some basic visualizations of the survey results, broken down by race.

#### Gender Diversity
Building off of the question discussed above for racial diversity, I plan for my second research question to be 'how does participation in outdoor recreation vary by gender?'. More specifically, are women more or less likely to participate in certain activities than men, and by how much? While this won't be truly representative of gender diversity in outdoor recreation due to the limitations described in the Data section above, I hope that it will at least give a ballpark idea of the extent of female participation. Even with significant limitations, I would still like to include this analysis since, as someone who identifies as female and participates extensively in outdoor activities, I am highly aware of the gender gap (the "shrink it and pink it" mantra of many gear makers is one particular constant annoyance of mine) and am passionate about making the outdoors more inclusive to gender minorities.

Similar to the analysis of race, the SCORP survey report gave a cursory analysis of particular activities with a marked difference between male and female participation (3), but did not go beyond that to include any statistical analysis. Here I plan to do the same analysis described above in the Racial Diversity section, but using 'male' and 'female' participants as the different categories.

## Tools
I plan to use python to complete all data processing and analysis for this project. The final deliverable will be a jupyter notebook containing all python code, results, and markdown annotation. Code comments and descriptions within the notebook will be sufficient to ensure complete reproducibility.

This data set is not so large that it could not be downloaded and stored in this GitHub repo; however, for convenience and best practices for reproducibility, I plan to use the Socrata API (5) to access the data. A small number of calls can be made to the API without an access token, but these requests are limited and subject to lower throttling limits. Therefore I plan to request an API token and will suggest that anybody replicating this analysis do so as well.

## References
1. https://oyasin.io/wp-content/uploads/2018/08/BEA-Outdoor-Rec-Industry.pdf
2. https://www.outsideonline.com/2196351/seven-open-letters-outdoor-industry
3. https://data.wa.gov/api/assets/C15614E8-ED66-4157-8C9F-3843053E0828?download=true
4. https://data.wa.gov/api/assets/DFA7D6A8-43F4-4D90-A933-15B4FF955FB1?download=true
5. https://dev.socrata.com/foundry/data.wa.gov/hzyw-na2k
