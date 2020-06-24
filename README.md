# NYC_Race-SAT

Academic success in high schools: What factors influence differences in SAT performance across New York City?

ABSTRACT

The SAT is a standardized test widely used for college admissions in the United States. The goal of this project was to identify any unintended patterns that would put certain groups at an disadvantage. This is an important step in making the US education system more equal for all. According the US Department of Education website, the challenge of ensuring educational equity is formidable.

In hopes to be more informed on this matter, I would like to know:

1. What factors influence differences in SAT scores and opportunities to attend certain colleges/universities?
2. Factoring in housing prices, where can one get the best high school education in New York City?
3. Using crime and US Household median income data to back up the safety scores

METHODS

This analysis used descriptive statistics and data visualizations to explore the following datasets on New York City high schools.

1. ![Sat scores](https://data.cityofnewyork.us/Education/2012-SAT-Results/f9bf-2cp4) for all NYC high schools in 2011-2012
2. ![School attendance information](https://data.cityofnewyork.us/Education/School-Attendance-and-Enrollment-Statistics-by-Dis/7z8d-msnt) -- Attendance information for each school in New York City
3. ![Class size](https://data.cityofnewyork.us/Education/2010-2011-Class-Size-School-level-detail/urz7-pzb3) - Information on class size for each school
4. ![Advanced Placement](https://data.cityofnewyork.us/Education/AP-College-Board-2010-School-Level-Results/itfs-ms3e) - Advanced Placement (AP) exam results for each high school (passing an optional AP exam in a particular subject can earn a student college credit in that subject)
5. ![Demographic information](https://data.cityofnewyork.us/Education/School-Demographics-and-Accountability-Snapshot-20/ihfw-zy9j) - Demographic information for each school
6. ![Graduation outcome](https://data.cityofnewyork.us/Education/Graduation-Outcomes-Classes-Of-2005-2010-School-Le/vh2h-md7a) - The percentage of students who graduated, and other outcome information
7. ![School surveys](https://data.cityofnewyork.us/Education/NYC-School-Survey-2011/mnz3-dyi8) - Surveys of parents, teachers, and students at each school
8. ![NYC Housing Data](https://dev.socrata.com/foundry/data.cityofnewyork.us/5ebm-myj7) -Department of Finance (DOF) maintains records for all property sales in New York City, including sales of family homes in each borough. This list is a summary of neighborhood sales for Tax Class 1, 2 and 3 Family homes.
9. ![NYC Crime Data](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i/data) - Filter the complaint dates fro the year 2011


The extract, transform, and load (ETL) portion was done as part of dataquests instructions and methodology.
