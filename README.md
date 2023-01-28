# PISA-Science-Scores-Project
What factors are related to 2018 international PISA science scores and could be used to predict countries or schools that will have 2025 PISA scores in the 25th percentile?
Countries or schools predicted to have low scores could be provided support to improve their science education. 

PISA (Programme for International Student Assessment) created by the Organisation for Economic Co-operation and Development (OECD) tests the skills and knowledge of 15-year-old students in reading, mathematics, and science every three years. PISA 2018 included a questionnaire to be completed by school principals asking for information about the schools. https://www.oecd.org/pisa/data/2018database/CY7_201710_QST_MS_SCQ_NoNotes_final.pdf

If there is a relationship between certain school factors from the questionnaire and PISA 2018 Science scores, the values of those factors in the future could be used to predict PISA Science scores. Support for science education could then be provided to be those schools or countries predicted to have low science achievement.

To determine if there a  relationship between school factors and science scores, Pearson correlation analysis will be followed by the generation of a linear regression model. Inputting the values of the linear regression model's predictor variables could generate a proxy for the PISA science scores during the 3 year interim between tests.

Data Sources:  
https://www.kaggle.com/datasets/prasertk/pisa-scores-20062018  
https://www.kaggle.com/datasets/dilaraahan/pisa-2018-school-questionnaire

Five variables were chosen to be included as independent variables in the multiple regression linear model based on having the highest absolute value of correlation coefficients.

36% of the variance in 2018 PISA science scores can be explained through an OLS Regression Model factoring in the following variables:  
SC064Q03TA (-0.44): Proportion of students' parents participating in local school government  
RATCMP2 (44.69): Proportion of available computers connected to the Internet    
SC004Q06NA (0.33): Number of data projectors available in the school  
SC004Q03TA (0.03) Number of computers for students connected to the Internet  
SC048Q02NA (0.69): Percentage of students in the school with special needs

The following linear regression model could be used to determine schools or countries in need of science education support in the 3 year interim between PISA tests:  
-0.4374*SC064Q03TA + 44.6893*RATCMP2 + 0.3340*SC004Q06NA + 0.0338*SC004Q03TA + 0.6850*SC048Q02NA + 414.7062=SCIENCE SCORE

With data from the 2022 PISA (the test was postponed by a year because of the pandemic), the model can be refined. 
