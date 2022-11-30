# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: SAT & ACT Data Analysis<br>
Author: Lee Wan Xian

---
## Executive Summary

The purpose of this project is to use exploratory data analysis to advise the admission board of a college in United States (US) on whether SAT or ACT test scores should be a mandatory admission requirement. There are 2 objectives for this analysis. First, it is to understand the relationship between SAT/ACT test scores and the retention rate of undergraduate students. Next, it is to understand the relationship of SAT/ACT participation rate and the general wealth of the respective states. There will also be a brief analysis on colleges who have mandatory SAT/ACT test requirements against those who do not.<br>

This analysis shows that there is no strong correlation between SAT/ACT test scores and the retention rate of undergraduate students as well as between SAT/ACT participation rate and the general wealth of the respective states. To add on, there is no significant impact that mandatory SAT/ACT test requirements leads to a higher or lower college applicants acceptance rate.<br>

In conclusion, we will recommend that SAT/ACT requirement should be left as an optional consideration for admission.

---
## Problem Statement

A college based in United States (US) is accessing the need to make SAT & ACT compulsory for college admissions. We are hired by the college admission board to assess how relevant SAT & ACT scores are in predicting students' ability to cope with the college curriculum & continue on to their sophomore year. As the college has multiple campuses across the country, the board is also interested to know whether poorer states are less likely to take up the standardized test, as compared to wealthier states.

---
## Data Dictionary

### SAT Participation Rate, ACT Participation Rate & Annual GDP by State Dataframe

|Feature|Type|Description
|---|---|---
|state|object|U.S. State Name
|sat_part_rate_2017|float|Participation rate of 2017 high school graduate who took SAT in their state
|sat_part_rate_2018|float|Participation rate of 2018 high school graduate who took SAT in their state
|sat_part_rate_2019|float|Participation rate of 2019 high school graduate who took SAT in their state
|act_part_rate_2017|float|Participation rate of 2017 high school graduate who took ACT in their state
|act_part_rate_2018|float|Participation rate of 2018 high school graduate who took ACT in their state
|act_part_rate_2019|float|Participation rate of 2019 high school graduate who took ACT in their state
|annual_gdp_2017|float|Real annual GDP of the state for 2017. Measured in millions of chained 2012 dollars
|annual_gdp_2018|float|Real annual GDP of the state for 2018. Measured in millions of chained 2012 dollars
|annual_gdp_2019|float|Real annual GDP of the state for 2019. Measured in millions of chained 2012 dollars
|mean_sat_part_rate|float|Average Participation rate of high school graduate who took SAT in their state across 2017 to 2019
|mean_act_part_rate|float|Average Participation rate of high school graduate who took ACT in their state across 2017 to 2019
|mean_annual_gdp|float|Average real annual GDP of the state across 2017 to 2019. Measured in millions of chained 2012 dollars

### College enrollment data by State Dataframe

|Feature|Type|Description
|---|---|---
|state|object|U.S. State Name
|statecode|object|U.S. State Abbreviation based on US Postal Code Standards
|retention_rate_ave|float|Average rate of freshman year students by state who continued on to their sophomore year
|sat_mid_score|float|Median SAT score of students accepted into college by state
|act_mid_score|float|Median ACT score of students accepted into college by state

### Acceptance rate for US Colleges Admission Dataframe

|Feature|Type|Description
|---|---|---
|school|object|Name of College
|test optional?|object|Yes: SAT/ACT are optional for acceptance into this college<br>No: SAT/ACT are mandatory for acceptance into this college
|number of applicants|int|Number of applications received by the college
|accept rate|float|Rate of students who applied & got accepted into the college

---
## Summary of Findings

**Student Retention Rate**

Our analysis shows that ACT scores are moderately good indicators to show how well students can cope and continue on with their sophomore year. However, SAT scores are weak indicators for the same purpose.<br>
It is good to mention that states with a higher median SAT/ACT score tend to have a higher student retention rate in general.

Variable|Correlation with 2019 Retention Rate|Correlation with 2018 Retention Rate|Summary
---|---|---|---
SAT Score|0.33|0.23|There is a weak positive correlation with Student Retention Rate
ACT Score|0.42|0.30|There is a weak to moderate positive correlation with Student Retention Rate

**Annual State GDP**

Our analysis shows that the relationship between SAT/ACT participation and the general wealth of the state is relatively weak.<br>
It is good to point out that 13 states with 100% ACT participation rate fall within the lower spectrum of annual GDP by state. This could be explained by the fact that some of these states made ACT mandatory for students to sit prior to applying for college. For instance, the state of Kentucky ([source](https://education.ky.gov/AA/Assessments/Pages/default.aspx)).

Variable|Correlation with Annual State GDP|Summary
---|---|---
SAT Participation Rate|0.24|There is a weak positive correlation with Annual State GDP
ACT Participation Rate|-0.27|There is a weak positive correlation with Annual State GDP

**Impact on acceptance rate if SAT/ACT were made mandatory**

From our analysis, there is no significant causal relationship on acceptance rate when it comes to SAT/ACT being made mandatory for college admission.<br> The factor that truly affects applicant acceptance rate will be the number of applications received by the college. The higher the number of applications received, the lower the acceptance rate.

Variable|Correlation with Acceptance rate|Summary
---|---|---
Number of Applicants with Mandatory SAT/ACT|-0.22|There is a weak negative correlation with acceptance rate
Number of Applicants without Mandatory SAT/ACT|-0.33|There is a weak negative correlation with acceptance rate

---
## Conclusion

From our preliminary analysis, SAT & ACT test scores does not have the ability to forecast the likelihood of a student being able to cope with the US college education. There is no strong justification that the retention rate of students will increase due to higher scores that the students had in their SAT or ACT. To add on, the wealth of the state is not a good indicator to gauge the participation rate of SAT/ACT in the state.

Further analysis can be done to assess the magnitude of SAT & ACT scores on predicting the student retention rate. For instance, the analysis can be done at college level instead of state level average. We can also analyse the impact that state regulations have on SAT or ACT participation rate.

---
## Recommendation

From our analysis so far, the college does not need to make SAT & ACT compulsory for college admissions. We recommend that SAT & ACT should be left as an optional admission requirement instead.

---
## Python Libraries

* Python = 3.8
* Pandas
* Numpy
* Matplotlib
* Seaborn

---
## Credits

1. College enrollment data by institution level, US Department of Education. ([Link](https://collegescorecard.ed.gov/data/)).
2. Annual GDP by State, Bureau of Economic Analysis. ([Link](https://apps.bea.gov/itable/iTable.cfm?ReqID=70&step=1)).