# Web Scraping Pipeline

A complete end-to-end web scraping pipeline built with **Python**, **BeautifulSoup**, **Playwright**, **Pandas**, and **SQLite**. This project demonstrates how to collect data from both static and dynamic websites, clean and transform the data, and store it in structured formats for further analysis.

## Project Overview

This project performs:

* **Static Web Scraping** using BeautifulSoup
* **Dynamic Web Scraping** using Playwright
* **Data Cleaning & Transformation** with Pandas
* **Data Storage** in CSV and SQLite Database
* **Automated Data Processing Pipeline**

The pipeline scrapes:

1. **Book Information**

   * Title
   * Price
   * Rating
   * Availability

2. **Quotes Information**

   * Quote Text
   * Author
   * Tags

---

## Technologies Used

| Technology     | Purpose                   |
| -------------- | ------------------------- |
| Python         | Core Programming Language |
| Requests       | HTTP Requests             |
| BeautifulSoup4 | Static HTML Parsing       |
| Playwright     | Dynamic Website Scraping  |
| Pandas         | Data Cleaning & Analysis  |
| SQLite         | Data Storage              |
| AsyncIO        | Asynchronous Execution    |

---

## Project Structure

text
web_scraping_pipeline/
│
├── web_scraping_pipeline.ipynb
├── books.csv
├── quotes.csv
├── scraped_data.db
├── README.md
└── requirements.txt

## Features

### 1. Static Scraping with BeautifulSoup

Scrapes book information from multiple pages of the Books to Scrape website.

Extracted fields:

* Book Title
* Price
* Star Rating
* Stock Availability

### 2. Dynamic Scraping with Playwright

Uses Playwright's headless browser to scrape JavaScript-rendered content.

Extracted fields:

* Quote Text
* Author Name
* Tags

### 3. Data Cleaning

The pipeline performs:

* Price conversion to numeric format
* Rating normalization
* Removal of special characters
* Missing value handling
* Text standardization

### 4. Data Storage

Cleaned data is exported to:

#### CSV Files

text
books.csv
quotes.csv
#### SQLite Database

text
scraped_data.db
Tables:
sql
books
quotes

## ⚙️ Installation

### Clone Repository

bash
git clone https://github.com/yourusername/web-scraping-pipeline.git
cd web-scraping-pipeline
### Install Dependencies
bash
pip install beautifulsoup4 requests playwright nest_asyncio pandas
### Install Playwright Browser
bash
playwright install chromium

## Running the Project
Open the notebook:
bash
jupyter notebook web_scraping_pipeline.ipynb
Run all cells sequentially.

The pipeline will:

1. Scrape book data
2. Scrape quote data
3. Clean datasets
4. Generate CSV files
5. Create SQLite database

## Database Schema

### Books Table
sql
CREATE TABLE books (
    title TEXT,
    price REAL,
    rating INTEGER,
    availability TEXT
);
### Quotes Table
sql
CREATE TABLE quotes (
    text TEXT,
    author TEXT,
    tags TEXT
);

##  Learning Outcomes

This project demonstrates:

* Web Scraping Fundamentals
* Static vs Dynamic Content Extraction
* Browser Automation
* Data Cleaning Techniques
* Data Engineering Basics
* SQLite Database Integration
* Asynchronous Programming in Python

##Future Improvements

* Scheduled scraping using Cron Jobs
* FastAPI endpoint for data access
* Docker containerization
* Data visualization dashboard
* PostgreSQL integration
* Cloud deployment (AWS/GCP/Azure)
* Scraping multiple websites simultaneously

Give it a star on GitHub and feel free to contribute!
