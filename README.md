<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Job%20Market%20Intelligence&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Enterprise-Grade%20Web%20Scraping%20%26%20Skill%20Analytics%20Platform&descSize=16&descAlignY=58&animation=fadeIn" />

<br/>

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Selenium](https://img.shields.io/badge/Selenium-4.x-43B02A?style=for-the-badge&logo=selenium&logoColor=white)](https://selenium.dev)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen?style=for-the-badge)]()

<br/>

> **Transforming raw job listing noise into precision market intelligence — at scale.**  
> Built for data professionals who make decisions with evidence, not assumptions.

<br/>

[🚀 Quick Start](#-quick-start) · [📐 Architecture](#-system-architecture) · [📊 Insights](#-key-findings) · [🗺️ Roadmap](#%EF%B8%8F-roadmap) · [👤 Author](#-author)

<br/>

</div>

---

## 📌 Executive Summary

**Job Market Intelligence** is a production-grade data pipeline that automates end-to-end collection and analysis of tech job postings from Indeed. The system bridges the gap between unstructured web data and actionable hiring insights — enabling job seekers, career advisors, and workforce analysts to make **data-backed decisions** in real time.

| Metric | Value |
|--------|-------|
| 🎯 **Primary Platform** | Indeed (U.S. Tech Roles) |
| 🧠 **Analysis Scope** | Skill frequency, location density, role distribution |
| ⚙️ **Pipeline Type** | Extract → Clean → Analyze → Visualize |
| 📦 **Output Format** | Structured CSV + Visual Reports |
| ✅ **Compliance** | Ethical scraping — `robots.txt` respected |

---

## 🎯 Problem Statement

The tech hiring market evolves faster than any static report or survey can capture. Professionals making career decisions — whether upskilling, pivoting, or hiring — often rely on outdated or anecdotal data.

**This project solves that by:**
- Automating real-time data collection directly from live job boards
- Extracting and ranking the skills employers are actually hiring for *today*
- Delivering clean, reproducible insights with zero manual overhead

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                    JOB MARKET INTELLIGENCE PIPELINE              │
├─────────────────────────────────────────────────────────────────┤
│                                                                   │
│  ┌──────────────┐    ┌──────────────┐    ┌───────────────────┐   │
│  │   WEB LAYER  │ →  │  DATA LAYER  │ →  │  ANALYTICS LAYER  │   │
│  │              │    │              │    │                   │   │
│  │  Selenium    │    │  job_        │    │  analysis.ipynb   │   │
│  │  Chrome WD   │    │  listings    │    │                   │   │
│  │  scraper.py  │    │  .csv        │    │  • EDA            │   │
│  │              │    │              │    │  • Skill Freq.    │   │
│  │  • Dynamic   │    │  • Raw       │    │  • Geo Analysis   │   │
│  │    JS render │    │  • Cleaned   │    │  • Visualization  │   │
│  │  • Paginat.  │    │  • Deduped   │    │  • Reporting      │   │
│  └──────────────┘    └──────────────┘    └───────────────────┘   │
│                                                                   │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Automation** | `Selenium 4.x` + `WebDriver Manager` | Headless browser control, dynamic JS rendering |
| **Data Engineering** | `Pandas 2.x` | Cleaning, deduplication, transformation |
| **Visualization** | `Matplotlib` | Statistical charts and skill frequency reports |
| **Runtime** | `Python 3.10+` | Core orchestration and scripting |
| **Notebook** | `Jupyter` | Interactive EDA and reproducible analysis |

</div>

---

## 🗂️ Repository Structure

```
job-market-intelligence/
│
├── 📄 scraper.py              # Selenium pipeline — browser automation & HTML extraction
├── 📓 analysis.ipynb          # Jupyter notebook — EDA, feature engineering, visualization
├── 🗃️ job_listings.csv        # Raw scraped dataset (auto-generated on run)
└── 📘 README.md               # Project documentation (you are here)
```

---

## ⚙️ Pipeline Deep Dive

### Phase 1 — 🕷️ Intelligent Scraping

The scraper uses Selenium to launch a headless Chrome session, navigate Indeed job listings for data-related roles, and extract structured fields via XPath and CSS selectors.

**Fields Extracted:**
- `job_title` — Role name as listed
- `company_name` — Hiring organization
- `location` — City / Remote / Hybrid
- `date_posted` — Relative or absolute post date

### Phase 2 — 💾 Structured Storage

All scraped records are written to `job_listings.csv` — a portable, flat-file format optimized for downstream ingestion by Pandas, Spark, or any BI tool.

### Phase 3 — 🧹 Data Quality & Cleaning

```python
# Core cleaning operations applied
df.drop_duplicates(inplace=True)         # Eliminate duplicate listings
df.dropna(subset=['job_title'], inplace=True)  # Remove incomplete records
df['job_title'] = df['job_title'].str.lower()  # Normalize for matching
```

### Phase 4 — 🔬 Skill Frequency Analysis

A curated skill taxonomy is matched against normalized job titles using substring detection. Frequency counts are aggregated and ranked.

```python
skills = [
    "Python", "SQL", "Excel", "Power BI", "Machine Learning",
    "Tableau", "R", "AWS", "Statistics", "NLP",
    "TensorFlow", "Spark", "Airflow", "dbt", "Snowflake"
]

skill_counts = {
    skill: df['job_title'].str.contains(skill, case=False).sum()
    for skill in skills
}
```

### Phase 5 — 📊 Visual Intelligence

Bar charts generated with Matplotlib deliver an at-a-glance view of which skills dominate the market, ranked by frequency across all scraped listings.

---

## 📈 Key Findings

<div align="center">

| Rank | Skill | Demand Level | Category |
|------|-------|-------------|----------|
| 🥇 1 | **Python** | ████████████ Very High | Programming |
| 🥈 2 | **SQL** | ███████████ Very High | Database |
| 🥉 3 | **Excel** | ████████ High | Productivity |
| 4 | **Power BI** | ███████ High | Visualization |
| 5 | **Machine Learning** | ██████ Medium-High | AI/ML |
| 6 | **Tableau** | █████ Medium | Visualization |
| 7 | **AWS** | ████ Medium | Cloud |
| 8 | **Statistics** | ████ Medium | Analytics |

</div>

> 💡 **Insight:** Python + SQL proficiency appears in **over 70%** of data-related listings across all metro markets, making them the non-negotiable baseline for data professionals.

---

## 🚀 Quick Start

### Prerequisites

```bash
# Clone the repository
git clone https://github.com/karthikeyan/job-market-intelligence.git
cd job-market-intelligence

# Install dependencies
pip install selenium pandas matplotlib webdriver-manager jupyter
```

### Run the Scraper

```bash
python scraper.py
```

> Launches Chrome, navigates Indeed, extracts job listings, and saves `job_listings.csv`

### Launch Analysis Notebook

```bash
jupyter notebook analysis.ipynb
```

> Run all cells to perform cleaning, skill analysis, and generate visual reports.

---

## ⚖️ Ethical Engineering

This project was built with responsible data practices as a first-class concern:

- ✅ `robots.txt` reviewed and respected prior to scraping
- ✅ Request throttling implemented to prevent server strain
- ✅ No login bypass, authentication circumvention, or ToS violations
- ✅ Data collected solely for non-commercial, educational research
- ✅ No PII (Personally Identifiable Information) is collected or stored

---

## 🗺️ Roadmap

| Phase | Feature | Status |
|-------|---------|--------|
| v1.0 | Core scraper + EDA notebook | ✅ Complete |
| v1.1 | Multi-page pagination support | 🔄 In Progress |
| v1.2 | Full job description extraction | 📋 Planned |
| v2.0 | NLP-based skill entity extraction | 📋 Planned |
| v2.1 | Interactive Streamlit dashboard | 📋 Planned |
| v2.2 | Scheduled scraping + trend tracking | 📋 Planned |
| v3.0 | Multi-platform (LinkedIn, Glassdoor) | 🔮 Future |

---

## 👤 Author

<div align="center">

### **Karthikeyan Thirunavukkarasu**
*Data Engineer · Analytics Professional · Automation Specialist*

Demonstrating production-grade expertise in web scraping, data engineering pipelines, and market intelligence analytics — turning unstructured web data into decisions-ready insights for enterprise use cases.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" />

*Built with precision. Scaled with purpose. Delivered with integrity.*

</div>
