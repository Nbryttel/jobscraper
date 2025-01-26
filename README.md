# Jobscrapper Database Schema and Automation

This repository contains SQL and Python scripts for a comprehensive Job Scraping and Analysis Database Schema. It is designed to facilitate job market analysis by storing scraped job offers and their metadata in a structured, scalable, and normalized manner. The integration of Python ensures seamless automation of scraping, processing, and data management.

## Tools used:
- SQL Server on Azure: For hosting and managing the job scraping database.
- Azure Data Studio: For query development, database management, and data exploration.
- Visual Studio Code (VS Code): For developing Python scripts with an enhanced coding experience and extensions.
- Python: For automating job data scraping, processing, and database interaction.
- Lucidchart: For designing the database schema and visualizing entity relationships.
- Excel: For exporting and sharing analyzed job data.

## As part of this project, the following skills were applied:

1. Database Design and Data Modeling:
- Designed a normalized relational database schema optimized for storing and analyzing job-related data.
- Defined clear relationships between tables using primary keys, foreign keys, and unique constraints.
2. Data Automation and Wrangling:
- Developed Python scripts in Visual Studio Code to automate the scraping of job postings from platforms like LinkedIn and Indeed.
- Wrote SQL queries to clean, transform, and prepare data for analysis.
- Automated workflows for regular updates and data integrity checks.
3. Data Analysis and Reporting:
- Analyzed job market trends, such as in-demand skills, industries, and salary ranges.
- Used SQL and Python to extract meaningful insights from the data.

## Project Architecture:
As a first step, the database architecture was carefully designed using Lucidchart, ensuring clarity, scalability, and adherence to normalization principles. The schema organizes data into logical tables with primary keys, foreign keys, and unique constraints, ensuring data integrity. Clear relationships between dimensions, fact tables, and bridge tables enable efficient storage and analysis of job-related data.

Below, you can see the schema, showcasing how dimensions, fact tables, and bridge tables interact:

## Features 
1. SQL Database Schema
- Dimension Tables: Store metadata such as locations, companies, job titles, skills, technologies, industries, and more.
- Source Table: The JobOffers table acts as the central repository for job details, including job descriptions, salaries, job links, and statuses.
- Bridge Tables: Enable many-to-many relationships, connecting job offers with related skills, technologies, responsibilities, and buzzwords.
- Fact Table: FactJobScraper aggregates job data for analytics and reporting.

2. Advanced SQL Features
- Triggers: Automate updates to job statuses and detect the language of job descriptions.
- Custom Functions: Dynamically classify job descriptions based on language and assign job categories.
- Validation and Constraints: Maintain data integrity by enforcing rules on numeric values and relationships.
- Indexes: Optimize query performance for frequent operations.

3. Optional Extensions
- Application Tracking: Track job applications with statuses like "Pending," "Submitted," or "Accepted."
- Job Categories: Dynamically categorize jobs based on titles and keywords for easier filtering and analysis.

## Python Integration 
Python played a crucial role in automating the data scraping and processing workflows for this project. Using tools like Selenium and BeautifulSoup, the script dynamically interacted with job platforms such as LinkedIn to extract detailed job postings, even from JavaScript-rendered pages. Python handled everything from parsing job titles, descriptions, locations, and company names to detecting the language of the job description using a custom keyword-based detection algorithm. Once scraped, the data was processed, cleaned, and inserted into the SQL database via libraries like pyodbc. Additionally, Python scripts were used to extract relevant insights from the database, export data to Excel for further use, and automate workflows to ensure the system remained up-to-date with new job postings. This seamless integration of Python ensured efficient data collection, preparation, and usability for further analysis.


