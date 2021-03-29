# School District Analysis
## Initial note to grader
I had some trouble with the output of my jupyter file, so I went to office hours today to get help from James. In the end, he restarted the kernel and cleared the output and suggested I do this again if it continued to show the wrong output (showing the old summary data despite my code for replacing the Thomas High School grade nine students being correct). This has continued to be an issue since, and I have had to restart the kernel repeatedly to try and get my file to show me the right output. I have my original file from the module that has not replaced the grade nine students and my challenge file that has replaced the grade nin students, yet when I run one, it often shows the output for the other. I have tried to get the right screenshots for each in order to compare the analysis from before and after, but there may be some errors, and if so, I apologize for the confusion.


## Overview of District Analysis
Maria is responsible for analyzing information for City School System. She has been tasked with investigating, reporting and presenting information on standardized testing data for the school system to inform discussions and strategic decisions at the school and district level. 
We have been asked to help Maria analyze data on student funding and student's standardized math and reading scores.
Our goal is to aggregate the data and showcase trends in school performance to inform decisions around budgeting. In order to complete this, we will produce the following deliverables:
-   A high-level snapshot of the district's key metrics, presented in a table format
-   An overview of the key metrics for each school, presented in a table format
-   Tables presenting each of the following metrics:
    -   Top 5 and bottom 5 performing schools, based on the overall passing rate
    -   The average math score received by students in each grade level at each school
    -   The average reading score received by students in each grade level at each school
    -   School performance based on the budget per student
    -   School performance based on the school size 
    -   School performance based on the type of school

During analysis, evidence of academic misconduct was uncovered that suggested that reading and math grades for Thomas High School ninth-graders had been altered. As such, we were asked to replace all relevant scores with NaNs, then repeat the analysis and provide a report on how removing these scores affected the overall analysis.

## District Analysis Results
Impact of removing Thomas High School ninth graders on:

 - **District Summary**:  As you can see below, before the grades for Thomas High School's [THS] ninth-graders were removed, 64.9% of students in the district passed both their math and reading tests.
 ![old summary](/Screenshots/Old_District_Summary.PNG)
After the THS ninth-graders were removed, the average math score for the district increased while the average reading score stayed the same. The percentage of students passing their reading and math tests increased 0.1-0.2 percent (as seen below). This brought the rate of passing students overall up to 65.2%
 ![new summary](/Screenshots/New_District_Summary.PNG)
 
 - **School Summary**:
  With regards to THS specifically, replacing the ninth-grade students pulled the percent of passing students up dramatically. Before the update, you can see (below) that only 66.9% of students passed the standardized math test, and 69.7% passed the reading test. Overall, only 65.1% of students passed both tests.
 ![old summary](/Screenshots/School_Summary_Old.PNG)
 After removing the grade nine students, however, these ratios improved substantially. As you can see from the output below, 93.3% of students from grades 10-12 passed the math test, and 97.3% passed the reading test. Overall, 90.1% passed both tests. The average scores on these tests changed each time I ran the code, which I think came as a result of whatever was going on with my jupyter notebook. This did not stop after I started a new jupyter notebook and restarting the kernel, and cleared all output, so I am not sure what happened and am unable to analyze these results.
 ![new summary](/Screenshots/School_Summary_New.PNG)



 - **Thomas High School's performance relative to other schools**:
 After removing the ninth graders from THS's scores, this jump in performance resulted in THS landing second amongst the rest of the schools in the district when ranked for performance. Before, it was in the middle of the group. 
  ![school performance](/Screenshots/New_Thomas_vs_other_schools.PNG)


 - **Math and reading scores by grade**:
 To analyze the math and reading scores by grade, I first created a table with the average scores of each grade grouped by the school to compare the districts' schools. While these should not have changed after removing the THS ninth graders (with the exception of there being a "NaN" in place of an average score for the THS ninth-graders), these scores did change slightly, and I was unable to figure out why. This is in line with the generally difficult time I had with my output.  
![Math scores by grade and school](/Screenshots/Math_scores_by_grade.PNG)
![Reading scores by grade and school](/Screenshots/Reading_scores_by_grade.PNG)

Due to the difficulty I had with my output, I decided to manually print out the mean math and reading grades calculated before and after removing the THS ninth graders to compare them. I hoped that if the issue was with my output, then manually printing would still produce reliable values. 
The printed means can be seen below. While the mean grades for all students in grades 10-12 remain the same, the mean math grade from ninth graders changed. The average math and reading grades from the updated file were lower than the original file. As I would run the two files (the original and the challenge file where I replaced the THS ninth graders), they were spitting out output that seemed to fit the opposite file, so I think that may have occurred here since I would expect the mean to be higher after the THS ninth-graders were replaced.

![old math means](/Screenshots/Old_math_grade_averages.PNG)
![new math means](/Screenshots/Updated_math_grade_averages.PNG)
![old reading means](/Screenshots/Old_reading_grade_averages.PNG)
![new reading means](/Screenshots/Updated_reading_grade_averages.PNG)

 - **Scores by school spending**:
After replacing the THS ninth graders, the overall passing % for schools that spent $630-644 increased from 63% to 64%. This suggests that THS falls within this spending range and pulled the percentage up for its cohort. 

![Old scores per spending average](/Screenshots/Old_scores_per_spending_average.PNG)
![New scores per spending average](/Screenshots/Updated_scores_per_spending_average.PNG)


 - **Scores by school size**:
Similarly to the school spending analysis, after replacing the THS ninth graders, the overall passing % for medium-sized schools increased from 91% to 92% which suggests that THS is a medium-sized school and pulled the percentage up for its cohort. 

![Old scores per school size](/Screenshots/Old_scores_per_school_size.PNG)
![New scores per school size](/Screenshots/Updated_scores_per_school_size.PNG)

 - **Scores by school type**:
 Given that THS is a charter school, it comes as no surprise that replacing the THS ninth graders resulted in the overall passing % for charter schools increasings from 90% to 91%. 
![Old scores per school type](/Screenshots/Old_scores_per_school_type.PNG)
![New scores per school type](/Screenshots/Updated_scores_per_school_type.PNG)

## District Analysis Summary



In summary, the replacement of scores for ninth-grade students at Thomas High School resulted in the overall passing percentage for schools that spend $630-644 per capita, medium-sized schools, charter schools and ninth-graders increased. This implies that the potential academic dishonesty that occurred at Thomas High School may have impacted the budgeting decisions made for the district in terms of where to apply funding cuts and increases. The misconduct had the largest impact in terms of the .3% reduction of the overall passing percentage for the entire district, which may have impacted the district's funding from analysis done on a federal level.  
