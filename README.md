## Web Scraping and Analysis of Job Postings
Project Overview

This project focuses on collecting and analyzing job postings from Indeed to understand current market demand for data-related roles and skills. The scraper extracts structured job information including job title, company name, location, and posted date. After collecting the data, it is cleaned, processed, and analyzed to identify the most frequently required technical skills.

The objective of this project is to demonstrate practical knowledge in web scraping, data preprocessing, and exploratory data analysis using Python.

Objectives

The primary goal of this project is to scrape job listings from Indeed and transform unstructured web data into meaningful insights. The project extracts job title, company name, location, and posting date. After structuring the dataset, skill frequency analysis is performed to determine which technical skills are most in demand in the job market.

Tools and Technologies Used

This project was developed using Python as the core programming language. Selenium was used to automate browser interaction and handle dynamic content loading. Pandas was used for data manipulation and cleaning. Matplotlib was used to create visualizations for skill demand analysis. WebDriver Manager was used to automatically manage the Chrome driver setup.

Project Workflow

The project begins with inspecting the Indeed job listings page using browser developer tools to identify relevant HTML elements containing job information. Selenium is then used to automate the browser and extract job title, company, location, and posted date from the listing page.

The extracted data is stored in a CSV file for further processing. During the data cleaning stage, duplicates are removed, missing values are handled, and text formatting is standardized. Job titles are converted to lowercase to simplify skill detection.

Skill analysis is performed by defining a list of commonly required skills such as Python, SQL, Excel, Power BI, and Machine Learning. The frequency of each skill appearing in job titles is calculated and visualized using bar charts.

Project Structure

The project directory contains the scraper script responsible for collecting data, the generated CSV file containing job listings, the analysis notebook for data processing and visualization, and the README file explaining the project.

Key Insights

The analysis shows that Python and SQL are among the most frequently required skills in data-related roles. Major metropolitan cities show higher concentrations of analytics and data positions. The overall skill demand trend aligns with current industry standards for data analyst and data science roles.

Ethical Considerations

This project was conducted responsibly by reviewing the website’s robots.txt file before scraping. Only a limited number of pages were accessed to avoid excessive requests. The scraper was implemented in a controlled manner without aggressive crawling.

How to Run the Project

Install the required dependencies using pip. After installing the necessary libraries, run the scraper script to collect job data and generate the CSV file. The generated dataset can then be analyzed using the provided notebook or any Python environment.

Future Improvements

Future enhancements could include adding pagination support to scrape multiple pages, extracting full job descriptions for deeper analysis, implementing natural language processing techniques for advanced skill extraction, and building an interactive dashboard for visualization.

Author

Karthik K

This project demonstrates practical experience in web scraping, data cleaning, and market skill analysis using Python.
