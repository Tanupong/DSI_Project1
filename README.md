# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis



### Contents:
- [Background](#Background)
- [Problem Statement](#Problem-Statement)
- [Datasets](#Datasets)
- [Data Dictionary](#Data-Dictionary)
- [Summary of Analysis](#Summary-of-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

However, many students feel obliged to take these exam as 2.2 Million test-takers completed the SAT while 1.8 million students took the ACT. It has been known that SAT is more popular on the East and West coast, and the ACT is reigning in the MidWest.

<p align="center">
<img src="/image/SAT-vs-ACT-popularity-by-state.png" width="700" />
</p>

[*source: https://crushthegretest.com/act-vs-sat/*](https://crushthegretest.com/act-vs-sat/)

There ia also a myth that an Ivy League school has SAT preference over ACT, however, that is not true. In regards to the geographic argument, Yale University, an Ivy League school, has an approximate 6% in-state undergraduate population. From the students they enrolled, 74% took the SAT and 45% took the ACT. That indicates some students took both. The reason comes from only that most of their students are coming from SAT dominated states (California and New York.)

The reason behind the state/geographic dominance of SAT is due to the fact that The College Board's founder are a group of a dozen colleges who are all on the east coast. While the ACT was developed at University of Iowa in the Midwest which both tests still have its dominance in its origin state till now.

Let's look at the registration Costs for SAT and ACT

|Fee type|Details|SAT Cost|ACT Cost|
|---|---|---|---|
|**Registration Fee**|The normal fee for each administration of the test you register for|\\$68  (\\$52 without essay)|\\$70  (\\$55 without essay)|
|**Late Fee**|Charged if you register after the regular deadline but before the final late deadline	|\\$30|\\$32|

[*source:https://blog.prepscholar.com/sat-cost-act-cost-and-how-to-save-money*](https://blog.prepscholar.com/sat-cost-act-cost-and-how-to-save-money)

It can be seen that the price of both test is very similar

Below is 2019 Median Household Income in the US.

<p align="center">
<img src="/image/median_hh_income.png" width="700"/>
</p>

[*source: https://www.census.gov/library/visualizations/interactive/2019-median-household-income.html*](https://www.census.gov/library/visualizations/interactive/2019-median-household-income.html)

In this study, we will explore how the trends has been for the last three years for each test, Nationwide and in top state where SAT is more favorable, to point out where should the board improve its marketing campaign to take over the competitor and make the most profit.


## Problem Statement

**Tracks statewide participation between SAT and ACT to recommend where should the board improve participation rates**

## Datasets

In this analysis, the datasets used are

* [`sat_2017.csv`](../data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](../data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv`](../data/sat_2019.csv): 2019 SAT Scores by State

* [`act_2017.csv`](../data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](../data/act_2018.csv): 2018 ACT Scores by State
* [`act_2019.csv`](../data/act_2019.csv): 2019 ACT Scores by State

* [`students_by_state.xlsx`](../data/students_by_state.xlsx): Number of students enrolled in public high schools in the United States in 2017
([*source*](https://www.statista.com/statistics/1036120/public-high-school-enrollment-state-us/))

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|object|sat.data,act.data|State where the data is collected|
|**participation_rate**|float|sat.data,act.data|the percent of number of people who took the test|
|**ebrw**|int|sat.data|Average Score in Evidence-Based Reading and Writing section|
|**math**|int|sat.data|Average Score in Math section|
|**total**|int|sat.data,act.data|Average Total Score in that state|
|**year**|int|sat.data,act.data|Year when data is collected|
|**no_students**|int|sat.data,act.data|Number of students enrolled in public high schools in grade 6in the United States in 2017|


## Summary of Analysis

1. Numbers of SAT takers increase significantly after 2016. However,There are many states that SAT is not popular resulting in low participation rates.
2. In Illinios, Colorado and West Virginia, the marketing campaign used is very effective. Since it can turn from very low SAT participation rate to become one of the highest SAT participation rate in the country. Its Strategies needs to be extended to other states with similar characteristics.
3. Connecticut, Delaware and Michigan have 100% SAT participation rates over the past three year while ACT performance in these 3 states are not very strong. Theses 3 states also needs to be study more to understand the key winning factors.

## Conclusions and Recommendations
Based on our problem statement, we found that
1. We should focus on Ohio and North Carolina by using strategies extracting for states mentioned above since they have the largest number of students and have similar characteristic to Illinios, Colorado and West Virginia.
2. Also focus on California and Texas by trying to use strategies from 'Suppress' group which have the most loyalty and popularity among students in their area.
