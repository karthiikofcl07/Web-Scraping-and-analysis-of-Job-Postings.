# 🔍 Job Market Intelligence — Web Scraping & Skill Analysis

> *Turning raw job listings into actionable market insights using Python, Selenium, and data analytics.*

---

## 📌 Overview

This project automates the collection and analysis of **data-related job postings from Indeed**, transforming thousands of unstructured listings into clean, structured datasets — and ultimately into clear answers about what skills today's employers actually want.

Whether you're a job seeker, career switcher, or researcher, this tool gives you a data-driven lens into the current tech hiring landscape.

---

## 🎯 Objectives

- **Scrape** job listings from Indeed using browser automation
- **Extract** structured fields: job title, company, location, and posting date
- **Clean & preprocess** raw data into an analysis-ready dataset
- **Analyze** skill frequency to identify what the market demands most
- **Visualize** findings through clear, informative charts

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| `Python` | Core programming language |
| `Selenium` | Browser automation & dynamic content handling |
| `Pandas` | Data manipulation, cleaning, and transformation |
| `Matplotlib` | Data visualization & charting |
| `WebDriver Manager` | Automatic Chrome driver management |

---

## 🗂️ Project Structure

```
job-market-intelligence/
│
├── scraper.py              # Selenium-based scraper — collects job listings
├── analysis.ipynb          # Jupyter notebook — cleaning, EDA, skill analysis
├── job_listings.csv        # Raw scraped dataset
└── README.md               # You are here
```

---

## ⚙️ How It Works

### 1. 🕷️ Scraping
Selenium automates a Chrome browser to navigate Indeed job listings. Using browser DevTools, relevant HTML elements are identified and extracted:
- Job Title
- Company Name
- Location
- Date Posted

### 2. 💾 Data Storage
Scraped data is saved to `job_listings.csv` — a flat, portable format ready for analysis in any Python environment.

### 3. 🧹 Data Cleaning
- Duplicate records removed
- Missing values handled gracefully
- Text standardized (lowercased for consistent keyword matching)

### 4. 🔬 Skill Analysis
A curated list of in-demand skills is matched against job titles:

```python
skills = ["Python", "SQL", "Excel", "Power BI", "Machine Learning",
          "Tableau", "R", "AWS", "Statistics", "NLP", ...]
```

Frequency counts are computed per skill and ranked to reveal demand trends.

### 5. 📊 Visualization
Bar charts built with Matplotlib clearly communicate which skills appear most across listings — giving instant, visual clarity on market demand.

---

## 📈 Key Insights

- **Python & SQL** dominate as the most in-demand skills across data roles
- **Major metro areas** (NYC, SF, Chicago, etc.) concentrate the highest volume of analytics positions
- Skill demand patterns closely align with industry benchmarks for **Data Analyst** and **Data Scientist** roles
- Emerging tools like **Power BI** and **Tableau** are rising fast alongside traditional skill sets

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install selenium pandas matplotlib webdriver-manager
```

### Run the Scraper
```bash
python scraper.py
```
> Launches a Chrome browser, scrapes job listings, and saves results to `job_listings.csv`

### Run the Analysis
Open `analysis.ipynb` in Jupyter and run all cells to generate cleaned data and skill visualizations.

---

## ⚖️ Ethical Scraping Practices

This project was built with responsibility in mind:

- ✅ Reviewed `robots.txt` before scraping
- ✅ Limited page requests to avoid server strain
- ✅ No aggressive or continuous crawling
- ✅ Data used solely for educational analysis

---

## 🔮 Future Improvements

- [ ] **Pagination support** — scrape across multiple result pages
- [ ] **Full job description extraction** — richer text for deeper analysis
- [ ] **NLP-based skill extraction** — move beyond keyword matching
- [ ] **Interactive dashboard** — Plotly/Dash or Streamlit visualization layer
- [ ] **Scheduled scraping** — track skill demand trends over time
- [ ] **Multi-platform support** — extend to LinkedIn, Glassdoor, and more

---

## 👤 Author

**Karthikeyan Thirunavukkarasu**

*Demonstrating practical expertise in web scraping, data engineering, and market analysis — turning messy web data into decisions-ready insights.*

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python" />
  <img src="https://img.shields.io/badge/Selenium-Automation-green?style=flat-square&logo=selenium" />
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat-square&logo=pandas" />
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square" />
</p>
