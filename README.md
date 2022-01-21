# School District Analysis

## Overview

### Initial Analysis

The School District provided datasets of schools and student data for an analysis on the performance of school's students based on thir math and reading grades.

After cleaning the data and summarizing it, reports on school spending, school size and school types were performed to assess the top and bottom schools according to the passing grades for math and reading.

### Further Analysis

The school board notified Maria evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. 

They want to repeat the initial school district analysis by replacing the math and reading scores for Thomas High School and describe how these changes affected the overall analysis.

### Resources
- Data source: The audit was performed on the file "election_results.cvs" provided by the Colorado Board of Election. The following image shows the structure of the file.

- Software use to perform the analysis: Python 3.7.11, Anacoda 4.11, Jupyter Notebook 6.4.6

## Results

### Replacements of grades

- The first step was to replace all the 9th graders math and reading scores for Thomas High School.

    ![grades replacement 9th graders at THS](/Resources/grades_replacement_nan.png)

- Obtained the following results:
    - Number of 9th grade students at Thomas High School: 461

    - Total students count without Thomas High School 9th graders: 38,709

    - District summary changed in the number of students and lightly in average scores and % of passing students as the following graphs show.  This is because 9th grade students at Thomas High School represent **1.2%** of total students.

    |Initial District summary |![Initial District Summary](/Resources/initial_district_summary.png)|
    |:------------------------|:-------------------------------------------------------------------|
    |Final District summary   |![New District Summary](/Resources/new_district_summary.png)        |

    - School summary.  By taking out grades of 9th grade students at Thomas High School, the % of passing math and reading were affected, as the number of students remained the same and grades for 9th grade students were set to NaN. This affected Thomas High School performance relative to the other schools.  So, we had to adjust the % of passing grades by taking into consideration only the grades and number of students for 10th to 12th graders at Thomas High School.

    |Initial School summary |![Initial District Summary](/Resources/initial_school_summary.png)|
    |:----------------------|:-----------------------------------------------------------------|
    |Final School summary   |![New District Summary](/Resources/new_school_summary.png)        |


    At the end, Thomas High School remained the top-2 school by performance as in the initial analysis.

### Impact of replacing the ninth-grade scores 

- Impact on Thomas High School overall grades.  By replacing 461 grades by NaN values, the passing percentages of this school dropped, because the student count included 9th graders. 

    |Initial THS grades summary |![Initial THS Summary](/Resources/initial_ths_grades.png)|
    |:--------------------------|:--------------------------------------------------------|
    |Final THS grades summary   |![New THS Summary](/Resources/new_ths_grades.png)        |

- Math and reading scores by grade. The only impact in average scores by grade is in the 9th grade for Thomas High School, as it was the only grades substituted by NaN values.

    |**Math scores by grade**                             |**Reading scores by grade**                                |
    |:---------------------------------------------------:|:---------------------------------------------------------:|
    |![math scores by grade](/Resources/math_by_grade.png)|![reading scores by grade](/Resources/reading_by_grade.png)|

- Scores by school spending. Thomas High School is in the spending range per student of $630-644. After having only considered 10th to 12th graders in the data, the average change was minimal.  

    |Initial Spending summary |![Initial Spending Summary](/Resources/init_speding_sum.png)|
    |:------------------------|:------------------------------------------------------------|
    |Final Spending summary   |![New Spending Summary](/Resources/new_speding_sum.png)  |

- Scores by school size. In the same toke, Thomas High School is in the Medium(1000-2000) size category. Change was minimal.

    |Initial Size summary |![Initial Spending Summary](/Resources/init_size_sum.png)|
    |:--------------------|:--------------------------------------------------------|
    |Final Size summary   |![New Spending Summary](/Resources/new_size_sum.png)     |

- Scores by school type.  Thomas High School is Charter School.  After modifications, there was no apparent change in the scores by school type.

    ![New Type Summary](/Resources/new_type_sum.png)

## Summary

We can summarize these for affections in updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs:

1. There were 461 students whose grades were replaced with NaNs. They represent 1.2% of Thomas High School total students. 
2. Total math average passing percentage changed from 75.0% to 74.8%
3. Total reading average passing percentage changed from 85.8% to 85.7%
4. Overall passing percentage changed from 65.2% to 64.9%
