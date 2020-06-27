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


### Hispanic Students vs SAT scores by school

![hispanic_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/hispanic_sat.PNG)

1. Schools with low average SAT scores and high percentages of Hispanic students are often named "International". These schools specialize on students with limited English skills thus these schools tend to score below average because the SAT tests both reading and writing.


2. Schools with high average SAT scores and low percentages of Hispanics are highly selective ('technical') public schools with prestigious reputations. Here's a list of schools from each borough with avg SAT > 1800:
            Manhattan - Stuyvesant High School, Bard High School Early College
            Bronx - Bronx High School and High School of American Studies at Lehman College
            Brooklyn - Brooklyn Technical School
            Queens - Queens High School for the Sciences at York College and Townsend Harris High School
            Staten Island - Staten Island Technical High School


This brings up another question of interest. Out of these high-performing schools (avg. SAT > 1800), what are the demographics?


### Demographic of NYC High Schools: "Elite" vs All.

![demo_school](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/demographic_nyc_schools.png)

Blacks and Hispanics are underrepresented in 'Elite Schools' whereas Asians and Whites are overrepresented. This could be attributed to certain groups having access to more resources.


### Correlation of gender and SAT Scores

![gender_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/gender_sat.jpg)

In the plot above, we can see that females have a positive correlation with SAT scores, whereas males have a negative correlation. However, neither correlation is extremely strong.


### Female vs. SAT scores by school

![female_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/female_sat.png)

I took a closer look at the schools with above average SAT scores (1400).

                        BARD HIGH SCHOOL EARLY COLLEGE
              PROFESSIONAL PERFORMING ARTS HIGH SCHOOL
                         ELEANOR ROOSEVELT HIGH SCHOOL
                                MILLENNIUM HIGH SCHOOL
                          TALENT UNLIMITED HIGH SCHOOL
                                    BEACON HIGH SCHOOL
    FIORELLO H. LAGUARDIA HIGH SCHOOL OF MUSIC & ARTS
                    BARD HIGH SCHOOL EARLY COLLEGE II
                           TOWNSEND HARRIS HIGH SCHOOL
    QUEENS GATEWAY TO HEALTH SCIENCES SECONDARY SCHOOL
          FRANK SINATRA SCHOOL OF THE ARTS HIGH SCHOOL

1. These schools appears to be very selective liberal arts schools that have high academic standards.

2. Only Manhattan and Queens high schools have > 60% female and scored above 1400. Females in the remaining boroughs may have limited access to good education. If we reduced female  % to 50 and kept > 1400 SAT Scores, it would only return 4 more schools in Brooklyn.

3. More than 50% of schools in Brooklyn and Bronx fall under the average SAT score (~1200).


### Advanced Placement (AP) Takers vs. SAT scores by school

![ap_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/ap_sat.png)


Advanced Placement (AP) is a program in the United States and Canada created by the College Board which offers college-level curricula and examinations to high school students. American colleges and universities may grant placement and course credit to students who obtain high scores on the examinations.


1. With SAT above 1400, there is a linear correlation between the AP Takers % and SAT scores. Upon more research, the school had high enrollments standards. Thus, students with higher academia would benefit more from these AP classes than other school.


2. It's suprising to see schools with high shares of AP takers exhibited near or equal the average SAT score. This draws another questions to why these schools exhibit such poor SAT scores given the high share of AP takers. We can use the Z-Score to determine which factors attribute more. The Z-Score represents, for a given value x of your numerical variable distribution, “how many standard deviations” it is from your variable mean. If Z-Score is positive, then your x value is above the mean. On the other hand, if your Z-Score is negative, then your x value is below that mean.

Otherwise, a high share of AP takers does not indicate a strong SAT score.


### AP Subject Matters: High AP, Low SAT & High AP, High SAT

![ao_subjects](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/ap_subject_sat.png)

Schools with high share of AP takers and low SATs offer a limited selection of courses. They mainly focus on history and literature; surprisingly English literature and composition is highly enrolled.


## NYC Housing Data

Read-in property sales data from 'NYC Open Data'-server following API documentation found on: https://dev.socrata.com/foundry/data.cityofnewyork.us/5ebm-myj7

#### Info about Dataset

Total Rows: 5979
Source Domain: data.cityofnewyork.us
Created: 6/14/2019, 8:17:31 AM
Last Updated: 4/17/2020, 12:38:45 PM
Category: City Government
Attribution: Department of Finance
Owner: NYC OpenData
Endpoint Version: 2.1


## Number of sales per year by home type

![num_sales_home_type](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/home_type_sales.jpg)

To no surprise, 1 family homes are the most common types of property sold.


## Reverse geocoding for insightful location features

Reverse geocoding is the process of back (reverse) coding of a point location (latitude, longitude) to a readable address or place name. Here's the [documenation](https://blog.batchgeo.com/new-feature-reverse-geocoding/). This was the first time I used this feature to get the names and detailed address from longitude and latitude coordinates.

Below are the steps on how I acquired the reverse geocodes

![geo_rev](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/rev_code_section.PNG)

### Added property data to school dataset

After merging the school and housing datasets, 40% of schools areas have property values associated with them.


## Property value vs. SAT score

![housing_val_sat](https://github.com/aclao89/NYC_Race-SAT/blob/master/Images/property_sat.png)


[Jamaica](https://www.niche.com/places-to-live/n/jamaica-new-york-city-ny/) and [Sheepshead Bay](https://www.niche.com/places-to-live/n/sheepshead-bay-new-york-city-ny/) have safety/respect scores of 7.4 and 7.9 with above average SAT scores in area under $1 million for a single family house.
[Woodhaven](https://www.niche.com/places-to-live/n/woodhaven-new-york-city-ny/), [Woodlawn](https://www.niche.com/places-to-live/n/woodlawn-new-york-city-ny/), [Flat-Bush Central](https://www.niche.com/places-to-live/n/flatbush-new-york-city-ny/), and [Cambria Heights](https://www.niche.com/places-to-live/n/cambria-heights-new-york-city-ny/) scored below 7.0 on safety/respect and more expensive than Jamaica and Sheepshead Bay.

[Staten Island Technical High School](https://www.siths.org/) in Oakwood Heights is the best pick in terms of housing price and superb average SAT performance. The housing price in Oakwood Heights are similar to Jamaica but Oakwood has a 300 points advantage on SAT.  
