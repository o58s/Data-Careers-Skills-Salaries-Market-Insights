# Data Careers: Skills, Salaries & Market Insights

## Introduction

As a data analytics enthusiast, I wanted to better understand the skills, roles, and salary trends shaping the data job market. I analyzed job market data to identify the skills most frequently requested by employers, how skill requirements vary across roles, and which skills are associated with higher salaries.

### Questions to Analyze

To understand the data job market, I asked the following:

1. **Do more skills get you better pay?**
2. **What’s the salary for data jobs in different regions?**
3. **What are the top skills of data professionals?**
4. **What’s the pay for the top 10 skills?**


### Excel Skills Used

The following Excel skills were utilized for analysis:

- **Pivot Tables**
- **Pivot Charts**
- **DAX (Data Analysis Expressions)**
- **Power Query**
- **Power Pivot**

### Data Jobs Dataset

The dataset used in this project contains real-world job market data for data-related roles collected in 2023. It was provided as part of Luke Barousse’s Excel data analysis course on YouTube and includes information on job titles, salaries, locations, employment types, and required skills. This project uses the dataset to explore trends in the data analytics and data science job market through Excel.

It includes detailed information on:

- **Job titles**
- **Salaries**
- **Locations**
- **Skills**

## Do more skills get you better pay?

### Skill: Power Query (ETL)

#### Extract

- I used **Power Query** to import and transform the original dataset (`data_salary_all.xlsx`) into two structured queries:

  -  **Data Jobs:** Contains the main information for each data-related job posting.
  - **Job Skills:** Contains the individual skills associated with each job posting, allowing for further analysis of skill demand across different roles.

#### Transform

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.
    - 📊 data_jobs_all






#### Load

- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.
    - 📊 data_jobs_al
 






### Analysis

#### Insights

- Skill requirements and salary: Job postings requesting a broader range of skills generally showed higher median salaries, with this pattern particularly visible among roles such as Senior Data Engineer and Data Scientist.
- Role and skill specialization: Roles such as Business Analyst generally required fewer technical skills and had lower median salaries, while more specialized data roles tended to require a broader combination of technical and analytical skills.


#### So What

- This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.

## What’s the salary for data jobs in different regions?

### Skills: PivotTables & DAX

#### Pivot Table 

- I created a PivotTable using the Data Model I created with Power Pivot.
- I moved the `job_title_short` to the rows area and `salary_year_avg` into the values area.
- Then I added new measure to calculate the median salary for United States jobs.
    ```
    =CALCULATE(
        MEDIAN(data_jobs_all[salary_year_avg]),
        data_jobs_all[job_country] = "United States")
    ```

#### DAX

- To calculate the median year salary I used DAX.

    ```
    Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
    ```

### Analysis

#### Insights

- Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.
- The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.


#### **So What**

- Salary benchmarking: These findings can help data professionals understand how salaries vary across roles and locations, providing a data-driven reference for career planning and evaluating potential job offers.


## What are the top skills of data professionals?

### Skill: Power Pivot

#### Power Pivot  
