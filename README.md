# The-Economics-of-US-Immigration---Insights-with-Tableau-

Data Overview
This project uses an H‑1B employment and salary dataset containing case decisions, wages, job titles, employer information, and geographic details. Each row represents a visa application submitted by a U.S. employer. The goal here is to understand the structure and analytic potential of the dataset.
What the data contains:
•	Case outcomes such as certified or denied.
•	Employer details including name, industry, and global presence.
•	Job attributes such as job title, SOC title, occupation group, and required education level.
•	Wage data includes prevailing wage, prevailing wage per year, and paid wage per year.
•	Work location includes city and state.
Key column categories:
•	Application: Case Number, Case Status, Case Received Date, Decision Date.
•	Employer Information: Employer Name, Employer Country, Employer Number of Countries, Industry.
•	Job & Role Attributes: Job Title, Job Title Subgroup, SOC Title, Occupation Group, Education Level Required, Full Time Position.
•	Work Location: Work City, Work State.
•	Wage Fields: Prevailing Wage, Prevailing Wage Per Year, Paid Wage Per Year.

Performance-related measures:
•	Case Status (certified vs denied).
•	Paid Wage Per Year and Prevailing Wage Per Year.
•	Differences between prevailing and paid wages.
•	Job demand by job sub‑group.
•	Geographic patterns in applications and wage levels.
Initial observations:
•	Some columns contain missing values (e.g., education level).
•	Wage fields include outliers and require standardization.
•	Job titles are highly skewed toward software engineering roles.
•	Dates need formatting for Tableau (string → date).
•	Geographic fields appear valid but may require spelling normalization.

Data Preparation Phase
This section summarizes all cleaning and transformation steps done by comparing the original salary dataset with the updated version.
Data cleaning performed:
•	Removed duplicate records present in the original dataset
•	Converted Case Received Date and Decision Date from string to proper date format
•	Standardized wage fields: Prevailing Wage Per Year and Paid Wage Per Year as numeric values
•	Renamed ambiguous or unclear columns for readability
•	Cleaned categorical fields including job titles, SOC titles, and occupation groups
•	Standardized Work City and Work State values for mapping
•	Removed rows where critical fields (Case Status or Paid Wage Per Year) were missing
•	Removed rows where all major fields were empty
•	Identified and flagged extreme wage outliers for further analysis
•	Cleaned inconsistencies in employer metadata, including global presence fields

Transformations:
•	Created calculated fields such as Wage Difference, Wage Ratio, Case Duration, and Wage Compliance Indicator.
•	Built additional fields like High Wage Flag, Employer Category (Multinational vs Domestic), and Standardized Job Title Groups.
•	Created parameters for Wage Threshold, Job Category Selection, State Selection, and Custom Date Range.
•	Created wage bins for Paid Wage and Prevailing Wage to support salary distribution analysis.
•	Standardized geographic fields for visualization (Work City, Work State).
•	Joined cleaned employer, job, and wage fields into a unified analysis-ready dataset.

Final dataset summary:
The updated Excel file is now clean, standardized, and validated for Tableau. It integrates wage information, visa outcomes, employer characteristics, job titles, and geographic fields into a single analysis-ready dataset.
Conceptual Modeling
Dashboard 1: US Visa Application Trends & Decision Metrics
Purpose: Explains the scale, trend, and decision behavior of US visa applications between 2008–2015.
Key Visualizations:
1. Year-wise Case Count Line Chart
2. Case Applications by Job Role - Bar Chart
3. US State Wise Applications - Map
4. Visa Class Processing Time Table

Dashboard 2: Employment & Visa Opportunity Analysis by City
Purpose: Highlights city-level opportunity clusters for tech and non-tech roles.
Key Visualizations:
1. Top Cities with High Visa Acceptance – Vertical Bar
2. Top 10 IT Hubs – Horizontal Bar
3. Top 10 Cities for Educators – Stacked Horizontal Bar
Dashboard 3: US Employment Analytics — Paid vs Prevailing Wage Trends
Purpose: Analyzes wage behavior, wage fairness, and employer competitiveness.
Key Visualizations:
1. Paid vs Prevailing Wage by Job Role – Dual Axis Combination Chart
2. Yearly Average Salary - Bubble Chart
3. Visa Class Wage Comparison Table
4. City-Level Scatter Plot (Paid vs Prevailing Wage)

Dashboard 4: Visa Application Outcomes & Employer Acceptance Patterns
Purpose: Identifies employer reliability, certification outcomes, and job role success rates.
Key Visualizations:
1. Case Outcome - Treemap
2. Top Employers with High Acceptance – Table Calculations
3. Highly Accepted Job Roles Pie Chart

Story 1: The Economics of Immigration: Visas and Wages in The U.S.
Purpose: Combines the four dashboards into a sequential analytical storyline.
The combined insight from all four dashboards yields a comprehensive immigration story. A broad overview of visa application trends in Dashboard 1, by job roles, states, and processing behaviors, is illustrated. City-level opportunity hubs for both tech and non-tech are emphasized in Dashboard 2. Dashboard 3 looks at paid versus prevailing wages as an assessment of fairness and competitiveness in compensation. In addition, Dashboard 4 explains the determinants of visa outcomes for employers and job roles, indicating who wins in the system. Combined, they offer an end-to-end look at visas, wages, employers, and geographic opportunities across the United States.
