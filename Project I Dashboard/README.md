# Excel Salary Dashboard  

![Data Science Salary Dashboard](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Data%20Science%20Salary%20Dashboard.jpg)  

## Introduction  

This data jobs dashboard was created to help job seekers explore salaries for their desired positions and ensure they are being adequately compensated.  

The data comes from an Excel course that provides a foundation in analyzing data using this powerful tool. It includes detailed information on job titles, salaries, locations, and essential skills, which are presented here.    

### Dashboard File  

You can access [my final dashboard in this Excel file](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Project%20I%20Dashboard/Salary%20Dashboard.xlsx).  

### Excel Skills Used  

The following Excel skills were utilized for this analysis:  

-📊 Charts  
-📐 Formulas & Functions  
-✅ Data Validation  

### Data Jobs Dataset  

The dataset used for this project contains real-world data science job information from 2023. It is available through my Excel course, which provides a foundation for analyzing data using Excel. The dataset includes detailed information on:  

- 👔 Job titles  
- 💰 Salaries  
- 📍 Locations  
- 🛠️ Skills  

## Dashboard Build  

### 📈 Charts  

🗠 **Data Science Job Salaries - Bar Chart**  

![Job Salaries](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Chart.png)  

- 🧰 Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.  
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.  
- 🗂️ Data Organization: Sorted job titles by descending salary for improved readability.  
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

🗺️ **Country Median Salaries - Map Chart**  

![Country Map](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Country%20Map.gif)  

- 🧰 Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- ✨ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas & Functions  

⚖️ **Median Salary by Job Titles**  

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🎛️ Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.  
- 🧩 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.  
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🎯 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

🗂️ **Background Table**  

![Median Salary](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Screenshot.png)  

🛠️📊 **Dashboard Implementation**  

![Job Title](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Job%20Title.png)  

🔢📅 **Count of Job Schedule Type**  

```    
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))  
```

- 🆕 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🎯 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

🗂️ **Background Table**  

![Job Schedule Type Sorted](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Screenshot%202.png)  
🛠️📊 **Dashboard Implementation**  

![Job Schedule Type](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboard%20Type.png)  

### ✅ Data Validation  

🎛️📋 **Filtered List**  

- 🧪 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
  - 👤 User input is restricted to predefined, validated schedule types
  - ❌ Incorrect or inconsistent entries are prevented
  - 👍 Overall usability of the dashboard is enhanced

![Data Validation](https://github.com/VAurelioIII/Excel-Project-Data-Analytics/blob/main/Images/Salary%20Dashboad%20Data%20Validation.gif)  

## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from an Excel course, it allows users to make informed decisions about their career paths by exploring how location and job type influence salaries.  
