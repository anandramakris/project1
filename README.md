# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Problem Statement

Michigan is the largest state where every high schooler in recent years has taken the SAT. At least some of those high schoolers would like to stay in Michigan rather than attending college elsewhere. Should students in Michigan who wish to stay in-state try harder than the average Michigander to do well on the SAT?

---

### Overview

The project takes a selection of Michigan colleges and statistically analyzes the 25th and 75th percentiles of the SAT scores of students admitted to them as of 2021. It attempts to correlate them with other statistics such as the acceptance rate and the number of applicants, and compares the percentiles to Michigan high school SAT averages from previous years.

---

### Datasets

#### Provided Data

* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))


#### Additional Data
* [`colleges.csv`](../data/colleges.csv): Tracking Covid-19 at U.S. Colleges and Universities ([source](https://github.com/nytimes/covid-19-data/blob/master/colleges/colleges.csv))

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**college**|*object*|ACT/SAT|The name of the college.|
|**test_optional**|*object*|ACT/SAT|Whether the SAT (or ACT) is optional when applying to the college.|
|**num_applicants**|*int*|ACT/SAT|The most recently reported statistic for the number of applicants to the college.|
|**accept_rate**|*float*|ACT/SAT|The most recently reported statistic for the fraction of applicants accepted to the college.|
|**sat_25**|*float*|ACT/SAT|The 25th percentile of SAT scores for students accepted at the college.|
|**sat_75**|*float*|ACT/SAT|The 75th percentile of SAT scores for students accepted at the college.|
|**state**|*object*|COVID|The state the college is located in. For this dataset, all colleges are in Michigan.|

---

### Conclusions & Recommendations

The ten Michigan colleges in the SAT & ACT dataset all have either higher or only slightly lower 25th percentiles of admitted SAT scores than the average Michigan high school student in each year from 2017 to 2019. In addition, their 75th percentiles are all much higher than the yearly Michigan averages. Thus, test-takers should strive to do much better than the average Michigander to get into any of them.

As there is a strong negative correlation between acceptance rate and SAT scores, students should try the hardest for the two highly selective colleges, the University of Michigan and Hillsdale College. They should aim for a perfect score if their first choice is the University of Michigan and at least 1500 if their first choice is Hillsdale. If their first choice is any of the other eight, aim for 1300, even though their acceptance percentages are all above 60%.

It is debatable whether the SAT should be taken at all, given how learning at home, especially without the proper resources, leads to students becoming far behind. But given Michigan's unique situation of requiring SAT scores on transcripts, it is worth the effort to do well because college admissions teams will look at the score.

---

### Outside Sources

The Michigan Merit Exam, which is required on high school transcripts and which has the SAT as a part, is discussed in further detail [*here*](https://detroit.chalkbeat.org/2021/6/25/22549509/michigan-sat-university-college).

Discussion of taking the SAT during the COVID-19 pandemic, including pro-SAT opinions by college counselors, is included [*here*](https://www.bridgemi.com/talent-education/will-coronavirus-curb-act-and-sat-admissions-tests-michigan-colleges).

Sources which detail specific code or mathematical topics are linked in the 'code/michigan-sat-analysis.ipynb' file.