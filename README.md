# Web-Scraping-and-analysis-of-Job-Postings.
📌 Project Overview

This project focuses on scraping job listings from Indeed and analyzing in-demand skills in the job market. The scraped data includes job title, company name, location, and posting date. After collecting the data, it is cleaned and analyzed to identify the most frequently required skills.

This project demonstrates practical knowledge in web scraping, data cleaning, and exploratory data analysis using Python.

🎯 Objectives

Scrape job listings from Indeed

Extract key fields:

Job Title

Company Name

Location

Posted Date

Clean and structure the collected data

Perform skill frequency analysis

Visualize the most in-demand skills

🛠 Tools & Technologies Used

Python

Selenium (for dynamic web scraping)

Pandas (data manipulation)

Matplotlib (data visualization)

BeautifulSoup (HTML parsing – initial testing)

WebDriver Manager

⚙️ Project Workflow
1️⃣ Website Inspection

Inspected Indeed job listings page using browser developer tools.

Identified HTML elements containing job information.

2️⃣ Web Scraping

Used Selenium to automate Chrome browser.

Extracted:

Job Title

Company

Location

Date Posted

Stored scraped data into a CSV file.

3️⃣ Data Cleaning

Removed duplicates

Handled missing values

Standardized text formatting

Converted job titles to lowercase for skill detection

4️⃣ Skill Analysis

Defined a list of common skills:

Python

SQL

Excel

Power BI

Machine Learning

Counted frequency of skills appearing in job titles.

5️⃣ Visualization

Created bar charts to display:

Most in-demand skills

Job distribution by location

📁 Project Structure
web-scraping-project/
│
├── scraper.py
├── indeed_jobs.csv
├── analysis.ipynb
└── README.md
📈 Key Insights

Python and SQL appear most frequently in data-related roles.

Certain cities show higher concentration of analytics roles.

Skill demand trends align with current data industry requirements.

⚠️ Ethical Considerations

Scraping was performed responsibly.

robots.txt was reviewed before scraping.

Limited number of pages were scraped.

No aggressive requests were made.

🚀 How to Run the Project

Install dependencies:

pip install selenium pandas matplotlib webdriver-manager

Run scraper:

python scraper.py

Open CSV file for analysis or run Jupyter Notebook.

💡 Future Improvements

Add pagination support

Extract full job descriptions

Perform advanced NLP-based skill extraction

Build an interactive dashboard

👨‍💻 Author

Karthik K

If you found this project useful, feel free to connect with me on LinkedIn and check out my other repositories.
