# School_District_Analysis
## Overview
A school board requested for grades to be reviewed for Thomas High School ninth grade scores in math and reading. The request is to check for dishonesty within the school using a previous district-wide analysis. The requested nineth grade scores will be removed from the analysis to observe any significant changes in the following:
  1. District Summary
  2. School Summary
  3. Math and reading scores.
  4. Scores by school student size, school type and school budget

## Resources 
- Data Sources: 
  - clean_students_complete.csv [found here](https://github.com/LauraHaq/School_District_Analysis/blob/main/Resources/clean_students_complete.csv)
  - schools_complete.csv [found here](https://github.com/LauraHaq/School_District_Analysis/blob/main/Resources/schools_complete.csv)
  - student_complete.csv [found here](https://github.com/LauraHaq/School_District_Analysis/blob/main/Resources/students_complete.csv)
- Software: Python 3.7, Jupyter Noteook

## Results
First step was successful in replacing all Thomas High School ninth grade class scores with not a number ("NaN") into a new DataFrame. No other scores for grades were changed.

![grades_replaced_nan](https://user-images.githubusercontent.com/86267773/126931538-8c4e0c10-9781-4493-b30e-20d5e0c778ac.png)
- Removing one grade level from one school in a district of 15 schools shows no change to district-wide data:
##### Initial District Summary
![initial_district_summary](https://user-images.githubusercontent.com/86267773/126927347-05dbc341-48a7-45e9-8e50-9ebe57fe2d65.png)
##### Adjusted District Summary
![adjusted_district_summary](https://user-images.githubusercontent.com/86267773/126926923-86c4469b-8d0c-4a9f-b1dc-506e4aea2ba5.png)

- Charter school averages and percent passing did not change:
##### Initial School Type
![initial_school_type](https://user-images.githubusercontent.com/86267773/126930452-320dcfaa-1853-44b9-aa97-7d104534511c.png)
##### Adjusted School Type
![adjusted_school_type](https://user-images.githubusercontent.com/86267773/126930430-5aab84e7-62b6-4874-b278-3ab15b44880d.png)

- Medium size school averages had no changes:
##### Initial School Size
![initial_schoolsize](https://user-images.githubusercontent.com/86267773/126930598-e34b42d0-c76a-44be-a09f-dd4a8e6b6c77.png)
##### Adjusted School Size
![adjusted_schoolsize](https://user-images.githubusercontent.com/86267773/126930563-7be761b1-cc4d-4971-b72e-27a4c4dcbcf0.png)

- School budget analyzed for spending per student passing did not show any changes:
##### Initial Spending Averages
![initial_spending](https://user-images.githubusercontent.com/86267773/126931015-4d6a74d7-557e-415a-8049-1eb941143a3b.png)
##### Adjusted Spending Averages
![adjusted_spending](https://user-images.githubusercontent.com/86267773/126930993-6970ef2a-2c04-456f-bf1a-42c32fe35a0b.png)

- On a school level changes are noticeable but not significant as Thomas School still holds a top 5 position in the district with "Overall Passing". Bottom schools are not affected. 
##### Initial Top 5 Schools
![initial_top_5](https://user-images.githubusercontent.com/86267773/126933540-9bda2658-015a-4060-a5c3-36385b26f26f.png)
##### Adjusted Top 5 Schools
![adjusted_top_5](https://user-images.githubusercontent.com/86267773/126933410-d0f72985-0aad-4496-81f0-93c57cf756bc.png)


## Summary
Overall, there are no significant changes to the results by removing Thomas High School's ninth grade scores from the district analysis. With a large number of students and only removing a small portion in comparison would lead me to not except one. However, with the school board questioning scores and my initial review of the data files, I would have expected there would be at least a slight decrease on a district level. To prove my hypothesis, I looked further into the analysis and found that there was a decrease in the initial reporting before formatting to decimal places:
![initial_district_summaryslightchange](https://user-images.githubusercontent.com/86267773/126927704-f149e720-721a-4350-8166-492343b03c1d.png)
![adjusted_district_summary](https://user-images.githubusercontent.com/86267773/126926923-86c4469b-8d0c-4a9f-b1dc-506e4aea2ba5.png)

The small changes in data also questioned my refactoring in regards using the replace function and referencing the correct DataFrames. However, the change of student counts for Thomas High School in the above data shows that the DataFrame was accurately being adjusted. With additional time I would be able to code calculations to confirm these numbers, as I did when confirming school size for Thomas High School after removing the ninth-grade class. 

![calculations](https://user-images.githubusercontent.com/86267773/126935403-62b6c0c9-5243-4e91-afd2-f677d29f2c26.png)

A final data point I would like to discuss is that the dollar amount per student did not change. To accurately calculate is to take the number of passing students removed in the 9th grade and multiply them by $638. Then to subtract at amount from the total budget then recalculate the number of passing students with what is left. It should come out to be the same.

In conclusion, I would not report back that there is no dishonesty occurring, but that I need to dive deeper into other grades at Thomas High School and possibly other schools to large variance of passing percentages. The code created could be used through all schools to report back in a short amount of time. I would begin by creating dataframes such as for Thomas High School's ninth grade and rerun codes to produce the same data to compare across the district. Also, run additional codes that calculations are accurate. 
