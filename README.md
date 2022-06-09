# School_District_Analysis_challenge
PyCitySchools with Pandas

## Overview
1. Open Jupyter Notebook files from local directories using a development environment.
2. Read an external CSV file into a DataFrame.
3. Format a DataFrame column.
4. Determine data types of row values in a DataFrame.
5. Retrieve data from specific columns of a DataFrame.
6. Merge, filter, slice, and sort a DataFrame.
7. Apply the groupby() function to a DataFrame.
8. Use multiple methods to perform a function on a DataFrame.
9. Perform mathematical calculations on columns of a DataFrame or Series.

## Purpose
- A school district asked for information on several key metrics by each school campus and by the district level. The main analysis focused on the performance of math and reading scores disaggregated several ways in preparation for a board meeting. However, after the school board reviewed the data, it was determined that the data from Thomas High School's 9th grade class was suspect of cheating. The school board asked for the data to be removed and analyzed again for a comparison.



# Results
## How is the district summary affected?

Orginal output:

<img width="700" alt="original output" src="https://user-images.githubusercontent.com/53058061/172738680-c7d6c7c9-47e5-48a6-9328-f5437cdbc598.png">



- The testing data of 9th grade students at Thomas High School was turned out to have null data, which recalculated the percentages of passing math, passing reading, and the overall passing. The total count of students did not change as that was run on the count of the student Ids, which was not affected.

New output:

<img width="699" alt="NewOut_districtsummaryaffected" src="https://user-images.githubusercontent.com/53058061/172738772-5c740f59-8ebc-4e3a-8940-7e8ef0c1529d.png">




- When comparing the charts, removing less than 500 test scores had a nominal impact on the almost 40,000 student data set. The change was less than  1% difference and the results would still round to the same number.


## How is the school summary affected?
- In the original output, Thomas High School started with a 91% overall passing rate, which was a concern to the school board for being too high. After calculating the total number of 10th - 12th grade students as the new denominator, the rest of the testing data was adjusted accordingly.

Original output:

<img width="748" alt="OG_schoolsummaryaffected" src="https://user-images.githubusercontent.com/53058061/172738808-01709083-e0c0-46b8-b87d-556914f444fa.png">



New output:

<img width="753" alt="new_schoolsummaryaffected" src="https://user-images.githubusercontent.com/53058061/172738813-a97c72a3-4aec-4582-b8e0-483257c1f3d7.png">


- Removing the 9th grade students from the data set had a big impact by dropping from 91% to 65% for the overall passing rate.

## How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

- In the original output, Thomas High School ranked 2nd in the district raising red flags.

Original output:

<img width="748" alt="OG_mathreadingscores" src="https://user-images.githubusercontent.com/53058061/172738856-d76bfa84-6664-4f23-90d5-94c5cfacd8d8.png">


- After adjusting the 9th grade data, Thomas High School ranked in the exact middle of 15 campuses at 8th from the bottom.

New output:

<img width="743" alt="new_mathreadingscores" src="https://user-images.githubusercontent.com/53058061/172738868-a2f99485-b2ae-4da6-89af-f16213d94c61.png">


# How does replacing the ninth-grade scores affect the following:

## Adjusted Averages using the Math and Reading Scores
- In the original analysis, Thomas High School had 83.6 math average and 83.7 reading average for the 9th grade tests. Now the scores have been replaced with null values and shows up in Python programming as NaN in the following charts.

New output for Average Math Scores/Adjusted Average Reading Scores

<img width="228" alt="avg_mathreadingscores1" src="https://user-images.githubusercontent.com/53058061/172738891-c1ddcd3d-a8f6-4db7-ae62-2554b5065937.png">

![Screen Shot 2022-06-08 at 7 44 17 PM](https://user-images.githubusercontent.com/53058061/172741723-69245031-83b0-4cc5-91ab-4f1c652e3283.png)



## Scores by School Spending 
- Thomas High School falls in the $630-$644/student spending range. (the hundredths place was needed to see the nominal changes)

Original output:

<img width="618" alt="OG_scoresbyschoolspending" src="https://user-images.githubusercontent.com/53058061/172738951-8476d050-7578-461e-a173-47d0a9592dcc.png">



New output:

<img width="620" alt="New_scoresbyschoolspending" src="https://user-images.githubusercontent.com/53058061/172738957-6dd32562-6f91-42ae-9eaa-1b3257c470cd.png">



- Small spending impact by changing the 9th grade scores.


## Scores by school size
- Thomas High School is defined as a medium sized school. (hundredths place was needed to see the nominal changes)

Orginal output:

<img width="563" alt="OG_scoresbyschoolsize" src="https://user-images.githubusercontent.com/53058061/172738979-7887cbc0-6e58-403f-ac23-717a7f552ebb.png">


New output:

<img width="560" alt="New_scoresbyschoolsize" src="https://user-images.githubusercontent.com/53058061/172738983-f636f92b-3e06-42a7-a82c-9d7b276fd905.png">


- Small impact by campus size due to changing the 9th grade scores.

## Scores by school type
- Thomas High School is a charter school type. (hundredths place was needed to see the nominal changes)

Orginal output:

<img width="531" alt="OG_scoresbyschooltype" src="https://user-images.githubusercontent.com/53058061/172739001-5363163a-5585-489a-a8f8-002186ec0d95.png">


New output:

<img width="531" alt="New_scoresbyschooltype" src="https://user-images.githubusercontent.com/53058061/172739015-3dfd1625-5446-49a7-8a2c-811702a099e9.png">


- Small impact by school type by changing the 9th grade scores.


# Summary
## Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

1. The overall passing rate for Thomas High School changed dramatically from 91% to 65%.

2. Thomas High School's ranking dropped from 2nd to 8th in the district of 15 campuses.

3. Data at the grade level will now show as "NaN" in reports for the 9th grade students at Thomas High School

4. In addition to the overall passing rate, the campus math and reading averages and passing percentages all saw shifts.

- The major changes will be seen in the lower views of the disaggregated data with little impact to the larger data views.




