This project provides an in-depth Human Resources (HR) Analytics study based on the IBM Employee Attrition dataset. The goal is to perform Exploratory Data Analysis (EDA) to identify and visualize the key factors (demographic, job-related, and performance) that contribute to employee turnover (attrition). The analysis leverages a foundational data science stack of SQL for efficient data management and Python for advanced analysis and visualization, ultimately yielding actionable insights for improved retention strategies.
🔎 Key Findings & Business Insights
Based on the analysis, several critical drivers of attrition were identified:
Overall Attrition Rate: The total attrition rate is approximately 16%.  
Departmental Risk: The Research & Development department accounts for the highest absolute number of employee departures.  
High-Risk Roles: Roles such as Sales Executive and Research Scientist show high attrition counts.  
Age and Tenure:
Employees who left had a lower average age (~39 years) compared to those who stayed (~43 years).  
Attrition is higher among employees with fewer years at the company.  
Workload Factor: Attrition is notably higher among employees who work Overtime.  
💻 Technical Stack and Implementation
This project uses a standard, powerful combination of tools for data analysis.
SQL (Data Management and Aggregation) 💾
SQL (Structured Query Language) is used for efficient data retrieval, filtering, and performing pre-calculations directly within the database.
Example: Query to Calculate Attrition by Department
-- Retrieve the number of employees who left ('Yes') for each department
SELECT
    Department,
    COUNT(CASE WHEN Attrition = 'Yes' THEN 1 END) AS Attrition_Count
FROM
    HR_Employee_Data
GROUP BY
    Department
ORDER BY
    Attrition_Count DESC;
    Contribution
Contributions are welcome! If you have suggestions for new features, optimized SQL queries, or alternative visualization techniques, please feel free to open an issue or submit a pull request.
