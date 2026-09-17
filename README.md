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

- I used **Power Query** to import and transform the original dataset (Dataset/data_jobs_salary_all.xlsx) into two structured queries:

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

- Data model: I created a relational data model by connecting the `data_jobs_all` and `data_jobs_skills` tables, allowing job-level information to be analyzed alongside the skills associated with each role.
- Data preparation: After cleaning and transforming the data in Power Query, I used Power Pivot to establish the relationship between the two tables and create a structured model for analysis.

#### Data Model

- I created a relationship between my two tables using the `job_id` column.

#### Power Pivot Menu

- The Power Pivot menu was used to refine my data model and makes it easy to create measures.


#### Insights

- Core analytics skills: SQL and Python emerged as two of the most frequently requested skills across data-related job postings, highlighting their importance in data extraction, analysis, and automation.
- Cloud skills: AWS and Azure also appeared frequently in job postings, reflecting the growing use of cloud platforms within modern data workflows and analytics environments.


#### So What

- Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.


## What’s the pay of the top 10 skills?

### Skill: Advanced Charts 

### Analysis

#### Insights

- Salary association: Skills such as Python, Oracle, and SQL were associated with higher median salaries in the dataset, highlighting their relevance across more technical and specialized data roles.

- Lower-salary skills: Skills such as PowerPoint and Word showed lower median salaries and lower skill likelihood, suggesting they were more commonly associated with roles with fewer specialized technical requirements.

### So What

- This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.

## Conclusion

As an aspiring data analyst, I developed this Excel-based project to explore trends in the data job market and understand how job requirements relate to salary. Using real-world job posting data, I analyzed job titles, salaries, locations, and in-demand skills. I used **Power Query, PivotTables, Power Pivot, DAX, and data visualizations** to clean, transform, model, and analyze the data.

The analysis identified patterns between skill requirements and salary levels, with technical skills such as **Python, SQL, and cloud technologies** appearing across a range of data-related roles. This project helped me strengthen my practical Excel and data analysis skills while demonstrating how data can be used to investigate career and job market trends.

