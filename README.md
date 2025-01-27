# Jobscrapper Database Schema and Automation

This repository contains SQL and Python scripts for a comprehensive Job Scraping and Analysis Database Schema. It is designed to facilitate job market analysis by storing scraped job offers and their metadata in a structured, scalable, and normalized manner. The integration of Python ensures seamless automation of scraping, processing, and data management.

This project also serves as an example for beginners who have never worked with SQL database design, database architecture, or Python automation. During the initial phases of designing the architecture and creating the first database scripts, I was accompanied by a former colleague who was new to these concepts.

It became an excellent learning opportunity for her to explore SQL, database management, and writing her first SQL scripts. Guiding her step-by-step through the process of designing the database architecture, explaining the relationships between tables, and creating the scripts allowed me to deepen my own knowledge. Her questions and feedback helped refine the project and provided valuable insights into teaching and collaboration.

I was able to mentor while simultaneously strengthening my skills in explaining complex topics, answering her questions, and leading her through the entire project. This project is therefore not only a functional system for job scraping and analysis but also a practical example for anyone new to database design and Python automation.

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

4. Mentoring and Knowledge Sharing.

## Project Architecture:
Below, you can view the Lucidchart diagram showcasing the database architecture designed for this project. It includes all the key components, such as dimension tables, fact tables, and bridge tables, with clear relationships defined by primary keys, foreign keys, and unique constraints. This visual representation provides a comprehensive understanding of how the database is structured to support efficient storage and analysis of job-related data.

## Guidance and Practical Learning
As part of the project, I had the opportunity to guide a former colleague who was new to SQL and database design. During our collaboration:

1. Practical Explanation: I used the Lucidchart diagram to explain the dependencies and relationships between the tables in real-time. For example, I showed how the FactJobScraper table connects to dimensions like DimCompanies and DimJobTitles, making the concept of fact and dimension tables more tangible.

2. Hands-On Practice: I encouraged my colleague to actively participate by asking questions and proposing changes to the architecture. Her queries about normalization, constraints, and table design helped refine the schema and provided a deeper learning experience.

3. Step-by-Step Walkthrough: I demonstrated how to translate the diagram into SQL scripts. Starting with table creation, we discussed constraints like CHECK, UNIQUE, and foreign key relationships, ensuring she understood both the purpose and implementation.
4. Iterative Learning: As the project progressed, I provided feedback on her SQL queries and scripts, helping her refine her skills while addressing real-world scenarios.

### A Collaborative and Interactive Approach
This collaborative approach significantly accelerated her understanding of SQL and database architecture. By combining the Lucidchart visualization with practical script-writing exercises, the project served as both a learning opportunity and a productive collaboration.

### Accessing the Architecture and Notes
The Lucidchart document includes:

- A detailed database schema diagram.
- My annotations explaining the relationships between tables.
- Her feedback on the project, along with my responses.
- This document can be a helpful resource for anyone learning SQL or database design for the first time. It provides not only the architecture but also a real-world example of how to approach building and understanding a database from scratch.

## Features of SQL Database
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


