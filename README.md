# Academic success in high schools: What factors influence differences in SAT performance across New York City?

## ABSTRACT

The SAT is a standardized test widely used for college admissions in the United States. The goal of this project was to identify any unintended patterns that would put certain groups at an disadvantage. This is an important step in making the US education system more equal for all. According the US Department of Education website, the challenge of ensuring educational equity is formidable.

In hopes to be more informed on this matter, I would like to know:

1. What factors influence differences in SAT scores and opportunities to attend certain colleges/universities?
2. Factoring in housing prices, where can one get the best high school education in New York City?
3. Using NYPD Crime Data, can we find any overlaps of high crime in poor performing schools?

## METHODS

This analysis used descriptive statistics and data visualizations to explore the following datasets on New York City high schools.

1. [Sat scores](https://data.cityofnewyork.us/Education/2012-SAT-Results/f9bf-2cp4) for all NYC high schools in 2011-2012
2. [School attendance information](https://data.cityofnewyork.us/Education/School-Attendance-and-Enrollment-Statistics-by-Dis/7z8d-msnt) - Attendance information for each school in New York City
3. [Class size](https://data.cityofnewyork.us/Education/2010-2011-Class-Size-School-level-detail/urz7-pzb3) - Information on class size for each school
4. [Advanced Placement](https://data.cityofnewyork.us/Education/AP-College-Board-2010-School-Level-Results/itfs-ms3e) - Advanced Placement (AP) exam results for each high school (passing an optional AP exam in a particular subject can earn a student college credit in that subject)
5. [Demographic information](https://data.cityofnewyork.us/Education/School-Demographics-and-Accountability-Snapshot-20/ihfw-zy9j) - Demographic information for each school
6. [Graduation outcome](https://data.cityofnewyork.us/Education/Graduation-Outcomes-Classes-Of-2005-2010-School-Le/vh2h-md7a) - The percentage of students who graduated, and other outcome information
7. [School surveys](https://data.cityofnewyork.us/Education/NYC-School-Survey-2011/mnz3-dyi8) - Surveys of parents, teachers, and students at each school
8. [NYC Housing Data](https://dev.socrata.com/foundry/data.cityofnewyork.us/5ebm-myj7) -Department of Finance (DOF) maintains records for all property sales in New York City, including sales of family homes in each borough. This list is a summary of neighborhood sales for Tax Class 1, 2 and 3 Family homes.
9. [NYC Crime Data](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i/data) - Dataset includes all valid felony, misdemeanor, and violation crimes reported to the New York City Police Department (NYPD) from 2006 to the end of last year (2017).

The extract, transform, and load (ETL) portion was done as part of dataquests instructions and methodology.

### Notebooks

1. Schools.ipynb - This notebook examined the data source from 1 to 8. The goal was to identify any unintended patterns that would put certain groups at an disadvantage

2. NYPD Crime 2001.ipynb - This notebook analyzed the crime rates and cross referenced the heat map with the schools with low safety/respect scores. This serves as a confirmation of unsafe neighborhoods which influences academic performance.


## Libraries used

![libraries](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/libraries.png)

## Data Analysis

### Correlation between student/teacher safety & respect score and SAT performance

![saf_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/saf_sat_corr.jpg)

There appears to be a correlation between SAT scores and safety, although it isn't that strong. It looks like there are a few schools with extremely high SAT scores and high safety scores. There are a few schools with low safety scores and low SAT scores. No school with a safety score lower than 6.5 has an average SAT score higher than 1500 or so. Unsafe environments could negatively influence good SAT performance.


### Correlation between survey responses and SAT scores

![survey_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/survey_sat.jpg)

Safety and Respect (saf_s_11 ~0.34) and student academic expectations (aca_s_11 ~0.34) have a moderate correlation with good SAT scores. It's also important to note the teachers' safety and respect score (saf_t_11 ~ 0.29) is relevant with good SAT scores. Overall, it makes sense when students and teachers feel safe and have trusting relationships, they can focus on providing a positive environment to achieve better academic results.


### Racial Differences in SAT Scores: Blacks and Hispanics are at high disadvantage

![black_hispanic](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/race_sat.jpg)

White and Asian students have a significant positive correlations with SAT scores, whereas  Black and Hispanic students have negative correlations with Hispanics being at a slightly higher disadvantage. This trends in the NYC dataset are in agreement with the achievement gaps among groups of students in the same time period (2011).  https://nces.ed.gov/nationsreportcard/studies/gaps/


### Hispanic Students vs SAT Score by School

![hispanic_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/hispanic_sat.PNG)

1. Schools with low average SAT scores and high percentages of hispanic students are often named "International". These schools specialize on students with limited English skills thus these schools tend to score below average because the SAT tests both reading and writing.


2. Schools with high average SAT scores and low percentages of hispanics are highly selective ('technical') public schools with prestigious reputations. Here's a list of schools from each borough with avg SAT > 1800:
            Manhattan - Stuyvesant High School, Bard High School Early College
            Bronx - Bronx High School and High School of American Studies at Lehman College
            Brooklyn - Brooklyn Technical School
            Queens - Queens High School for the Sciences at York College and Townsend Harris High School
            Staten Island - Staten Island Technical High School


This brings up another question of interest. Out of these high-performing schools (avg. SAT > 1800), what are the demographics?
