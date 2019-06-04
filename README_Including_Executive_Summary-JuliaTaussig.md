## Project 1: Standardized Testing, Statistical Summaries and Inference

### Overview
For this project, the aim was to inspect 2017 and 2018 state participation rate data and state average SAT and ACT score data and to identify trends in the data.  Another aim was to combine the data analysis with outside research to identify likely factors influencing ACT and SAT participation rates and scores in various states.  

### Problem Statement
The new format for the SAT was released in March 2016. At the College Board, we aim to track statewide participation and to carefully decide where money is best spent to improve SAT participation rates. During this project, data and outside research will be used to make recommendations about how the College Board might work to increase the participation rate in states such as Iowa.


### Executive Summary

### Repository Structure / Contents:
 - Data in the "data" folder/repository: act_2017.csv, sat_2017.csv, combined_2017.csv (contains cleaned ACT and ACT data for 2017), act_2018.csv, sat_2018.csv, and final.csv (the cleaned and combined 2017 and 2018 ACT and SAT data)
 - Code in the "code" folder: "Project1-DataAnalysisNotebook-JuliaTaussig": Jupyter Notebook containing data cleaning and analysis 
 - Project1_Presentation_JuliaTaussig.pdf: Presentation including data analysis and recommendations

### Data Collection
 - 2017 ACT data (including state participation rates and state average subject (English, Math, Reading, and Science) scores and composite scores): used the following source: Edwards, Halle. <https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows>
 - 2017 SAT data (including state participation rates and state average subject (Evidence-Based Reading and Writing (EBRW) and Math) scores and total scores): used the following source: Sundquist, Kate. <https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/>
 - 2018 ACT data (including state participation rates and state average composite scores): used the following source: ACT, Inc. <http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf>
 - 2018 SAT data (including state participation rates and state average subject (EBRW and Math) scores and total scores): used the following source: College Board. <https://reports.collegeboard.org/sat-suite-program-results/state-results>
 
### Ethical Considerations
 - The data collected will be used to collect information and to make internal decisions at the College Board.  This data does not include personal identifiers of individual students.
 
### Exploratory Data Analysis
 - Data Importing/Cleaning: 
     - The 2017 data was supplied by General Assembly (in act_2017.csv and sat_2017.csv).  The data was imported as dataframes, the values were checked, typos were found when comparing the data to the sources of the data, and values incorrectly input were corrected.  
     - The datatypes were checked and changed to appropriate datatypes (for example, percentages, such as 30%, were changed to proportions, such as 0.30, which are float datatypes).  The 2017 ACT and 2017 SAT data was organized as a dataframe, and the columns were renamed for clarity.  Unnecessary rows were removed.  The 2017 ACT and 2017 SAT data were combined to one dataframe, and the data was saved in a csv as combined_2017.csv.
     - The 2018 ACT and SAT data were manually translated into csv files (with help from Anna Haas).  The files are called act_2018.csv and sat_2018.csv.
     - The 2018 ACT and SAT data were then imported as dataframes and cleaned so each column included series of appropriate datatypes. The 2018 ACT and SAT dataframe columns names were renamed to increase clarity.
     - Both the 2017 and 2018 dataframes were combined.  The final dataframe was then saved in the data repository as final.csv.
     - A data dictionary was created for reference.
 - Summary statistics for all numerical variables were inspected.  A function to calculate standard deviation was created and used to inspect standard deviations of numerical variables (these values were verified using the NumPy package's standard deviation method)
 - Highest and lowest state participation rates for the 2017 and 2018 ACT and SAT were inspected (the sorting method was used).
 - Highest and lowest average total/composite scores for the 2017 and 2018 SAT and ACT were inspected (the sorting method was used).
 - States with 100% participation on a given test that had a rate change year-to-year were inspected.  Note that Anna Haas helped with masking work.  It was challenging to set up the mask, but it worked after speaking with Anna.
 - States that had >50% participation on both ACT and SAT tests either in 2017 or 2018 were inspected.  Note that Anna Haas helped with masking work.  It was challenging to set up the mask, but it worked after speaking with Anna.
 - Data Visualization: 
     - A heatmap was used to visualize whether variables correlated with each other. The redundant upper triangle of the heat map was removed to increase clarity.  The title of the heatmap was added with help from Anna Haas.
     -A custom function was built to creat histograms.  It was a challenge to build the function, but it saved time when the function was called several times to inspect the following:
         - Distributions of state participation rates for the ACT and SAT in 2017 and 2018, 
         - Distributions of math scores for the 2017 and 2018 SAT and  2017 ACT (note that 2018 ACT state average math scores were not given), and
         -Distributions of reading/verbal scores for the 2017 and 2018 SAT and the 2017 ACT (note that 2018 ACT state average  English and reading scores were not given)
     - A custom function was built to create scatter plots to visualize the following:  
         - SAT vs. ACT math scores for 2017
         - SAT vs. ACT verbal/reading scores for 2017
         - SAT vs. ACT total/composite scores for 2017
         - Total scores for SAT 2017 vs. 2018
         - Composite scores for ACT 2017 vs. 2018
     - Boxplots were created to visualize distributions of each numeric variable.  It was a challenge to utilize the Seaborn package to create the boxplots.  Outliers were not shown outside of the boxplot whiskers.  It would be helpful to determine why this happened.
     - To increase understanding of distributions and their skews, histograms were created for every numerical variable, and means and medians were calculated and compared for each numerical variable.
     - The following varibale data were sampled and averaged 1000 times (the mean of each sample set was taken) to create plots illustrating the Central Limit Theorem can be applied to non-normal data to create normal distributions which can be used to estimate values: 2017 and 2018 ACT and SAT applicable/available state average math, reading, and participation rates
     - Statistical inference of SAT and ACT participation rates in 2017 was not conducted because the data was not randomly sampled from a large population (and there were no control groups given).
     - Statistical inference/comparison of 2017 SAT and ACT math scores was not conducted because the data was not randomly sampled from a large population, and the SAT and ACT scores were scaled differently (and there were no control groups given). 
     - Further hypothesis tests to compare variables of interest in the dataset were not performed because it was not appropriate.
     - Outside research was conducted and is described in the Jupyter Notebook called "Project1-DataAnalysisNotebook-JuliaTaussig."
     - Recommendations and conclusions are below and in the Jupyter Notebook called "Project1-DataAnalysisNotebook-JuliaTaussig." 
 
 ### Recommendation:
 Based on exploration of the data, my key takeaway is that state legislation can help to significantly increase SAT and/or ACT participation.  As ACT or SAT participation rates increase, average state ACT or SAT scores can decrease.  I would recommend that if states find ACT and SAT participation rates important, it would be beneficial to require or to at least fund and hold test days at schools.  Even if an increase in ACT or SAT participation rate increases the variety of students who take the tests and may decrease state average scores, it is great to provide opportunities to students to take the ACT and SAT and then to focus on increasing state average scores in the long run.

For example, Iowa has one of the lowest SAT participation rates (and decent but not great ACT participation rates).  Iowa also has the third highest average SAT score (probably because most of the students who take the SAT are students who care about college admission and take both the ACT and SAT).  Students in Iowa are required to take the Iowa Assessments from 3rd grade to 11th grade.  I recommend that the College Board (the organization that administers the SAT) work with the Iowa Board of Education to either require students (11th graders or graduating seniors) to take the SAT or to require the students to choose to take either the SAT or ACT).  This has been shown to help other states such as Illinois to approach or reach 100% SAT participation.  Another approach is to host test days at schools during which students can take the SAT at no expense to them. Test days or a requirement to take the SAT could provide opportunities to students from low-income families (or generally help students who may not have time or money to take the SAT outside of school hours). 

### Conclusion:
The analysis of the ACT and SAT state participation rates and state average scores was infomative.  

It would help to have the following data to better inform investigations:
 - Anonymous data for each student in each state to increase ability to conduct statistical inference 
 - Percentage of students who take the ACT and the SAT instead of one or the other (and percentage of students who take neither the SAT or ACT to verify data)
 - ACT and SAT participation rate and score data from more years (it would be interesting to see trends from 2000-2016 and then to see trends after the SAT format changed in the spring of 2016)
 - 2018 average state ACT subject scores (English, math, reading, and science scores)
 - Survey data about students' opinions about why they prefer to take the SAT, whether they prefer to take the ACT, why they prefer to take both the SAT and ACT, or why they prefer to take neither the SAT nor the ACT
 - Data regarding college and university ACT and/or SAT requirements 
 - Graduation rates for each state
 
 ### Sources:
ACT, Inc. <http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf> 

College Board. <https://reports.collegeboard.org/sat-suite-program-results/state-results> 

Des Moines Public Schools.  <https://www.dmschools.org/academics/iowa-assessments/> 

Edwards, Halle. <https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows> 

Gewertz, Catherine, <https://www.edweek.org/ew/section/multimedia/states-require-students-take-sat-or-act.html>

Hawaii State Department of Education. <http://www.hawaiipublicschools.org/ConnectWithUs/MediaRoom/PressReleases/Pages/2017-ACT-Results.aspx> 

<https://www.google.com/search?q=sat+picture&source=lnms&tbm=isch&sa=X&ved=0ahUKEwj4zeTFxPHgAhWwna0KHdC5D9YQ_AUIDigB&biw=1200&bih=537#imgrc=rMvwPmFb_wXDqM:>

Sundquist, Kate. <https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/> 

Woods, Richard. <http://www.gadoe.org/Curriculum-Instruction-and-Assessment/Assessment/Pages/Georgia-Milestones-Assessment-System.aspx> 