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
1. web_scraping_pipeline/
   a. web_scraping_pipeline.ipynb
   b. books.csv
   c. quotes.csv
   d. scraped_data.db
   e. README.md
   f. requirements.txt

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

# Output 
1. Step 0: Install dependencies
    <img width="727" height="107" alt="image" src="https://github.com/user-attachments/assets/ffd2ba65-42cd-48d8-a049-fef3dd4cd8d6" />
1. Step 1: BeautifulSoup scrape (books.toscrape.com, 5 pages)
    <img width="782" height="352" alt="image" src="https://github.com/user-attachments/assets/fa7a8169-6c1d-471e-ae99-dbcbcf34b4ce" />
2. Step 2 : Playwright scrape (quotes.toscrape.com/js,)
   <img width="846" height="292" alt="image" src="https://github.com/user-attachments/assets/965e390d-65d1-4bf6-bb49-f706eb3c84d7" />
3. Step 3: Cleaning
    <img width="877" height="445" alt="image" src="https://github.com/user-attachments/assets/549001ab-6a05-406d-8a56-d7ec676f1e0c" />
4. Step 4: Save + SQLite sanity check 
    <img width="851" height="260" alt="image" src="https://github.com/user-attachments/assets/5cdd5a88-2300-4d88-88bb-e3b8bd48b98d" />

Give it a star on GitHub and feel free to contribute!
