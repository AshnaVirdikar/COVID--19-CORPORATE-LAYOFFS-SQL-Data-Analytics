# COVID--19-CORPORATE-LAYOFFS-SQL-Data-Analytics
# Project Overview 
This project analyzes layoffs data from 2020 to 2023, covering the period during and after the COVID-19 pandemic. Using SQL for data cleaning and exploratory data analysis (EDA), the project examines trends in workforce reductions across companies, industries, countries, and time periods. The dataset contains 2,931 records of layoff events from companies worldwide.

# Technical Stack

Database: MySQL
Primary Techniques: Window functions, CTEs, aggregations, joins, data type conversions
Dataset: 2,931 records covering 2020-2023

# Goals
Clean and standardize layoffs data to ensure accuracy and consistency
Identify trends in layoffs across different dimensions (time, geography, industry, company stage)
Discover patterns in workforce reductions during the pandemic period
Rank companies by layoff severity to understand which organizations were most affected
Calculate rolling totals to visualize the cumulative impact over time

# Key Performance Indicators (KPIs)
Total Layoffs: Sum of all employees laid off across the dataset
Maximum Single Layoff Event: Largest number of employees laid off in one event (12,000 from Google in 2023)
Average Layoffs per Company: Mean number of employees affected per layoff event
Percentage Laid Off: Proportion of workforce affected (up to 100% for companies that closed)
Companies with 100% Layoffs: 116 companies that completely shut down
Layoffs by Year: Temporal distribution showing pandemic impact timeline
Top 5 Companies per Year: Annual ranking of companies with highest layoffs
Rolling Monthly Total: Cumulative layoff count tracked month-over-month

# Features
1. Data Cleaning Process

Duplicate Removal: Identified and removed duplicate records using window functions and row numbering
Data Standardization:

Trimmed whitespace from company names
Consolidated industry categories (e.g., 'Crypto Currency' → 'Crypto')
Standardized country names (removed trailing periods)
Converted date strings to proper DATE format


Null Value Handling: Populated missing industry values where possible using company name matching
Data Validation: Removed records with no actionable layoff data (null total_laid_off AND percentage_laid_off)

2. Exploratory Data Analysis (EDA)
Basic Analysis:

Min/max/average layoffs calculations
Identification of complete company closures (100% workforce reduction)
Funds raised by bankrupt companies

Aggregated Insights:

Top 10 companies by total layoffs
Layoffs grouped by location, country, industry, and company stage
Year-over-year comparison of layoff volumes

Advanced Analysis:

Rolling monthly totals of layoffs using CTEs and window functions
Year-over-year company rankings using DENSE_RANK
Top 5 companies with highest layoffs per year
Temporal trends showing pandemic impact progression

# Key Insights
Company-Level Findings

Google had the largest single layoff event with 12,000 employees in 2023
116 companies completely shut down (100% workforce reduction) during this period
Twitter laid off 3,700 employees in 2022 despite having raised $1.29 billion in funding

Industry and Geographic Trends

Significant concentration of layoffs in the tech sector
SF Bay Area and major tech hubs experienced the highest layoff volumes
United States led globally in total layoffs

Financial Context

Many well-funded companies still conducted massive layoffs
HOOQ raised $95 million before going bankrupt
Startup stage companies were particularly vulnerable to complete closure

# Conclusions
This analysis reveals the profound impact of the COVID-19 pandemic on global employment, with several key takeaways:

Scale of Impact: The dataset captures nearly 3,000 layoff events affecting hundreds of thousands of workers across multiple industries and countries

Tech Sector Vulnerability: Despite being positioned for remote work, the technology sector experienced disproportionate workforce reductions, suggesting business model challenges beyond pandemic logistics

No Company Too Big: Even tech giants with massive resources (Google, Twitter) conducted significant layoffs, indicating systemic economic pressures

Startup Fragility: Over 100 companies completely shut down, highlighting how economic uncertainty disproportionately affected early-stage ventures regardless of funding

Extended Timeline: Layoffs continued well into 2023, demonstrating that workforce impacts outlasted the immediate health crisis
