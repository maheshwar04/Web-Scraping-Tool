# 🔍 Web Scraping Tool (Python + SQLite3)

## 📌 Overview  

This script scrapes **paragraphs** (`<p>` tags) from a given website and stores them in an **SQLite database**. It clears old data before inserting fresh content, ensuring efficiency.  

## ⚙️ Setup & Installation  

1️⃣ Install dependencies: `pip install requests beautifulsoup4`  

2️⃣ Run the script: `python scraper.py`  

3️⃣ Verify stored data in SQLite: `sqlite3 scraped_data.db` then `SELECT * FROM scraped_content LIMIT 5;`  

## 📝 Features  

✔ Scrapes **paragraphs** from any website  ✔ Stores data in **SQLite3** database  ✔ **Drops table** before inserting fresh data  ✔ Optimized for **efficiency & error handling**  

## 🔍 How It Works  

1. Fetches website HTML using `requests` 2. Extracts `<p>` tags using `BeautifulSoup` 3. Drops old table and creates a fresh one 4. Saves new paragraphs into SQLite 5. Prints execution time for efficiency check  

## 📌 Example Output (Terminal Preview)  

✅ Connected to database: scraped_data.db  🗑️ Dropped existing table!  ✅ Page loaded successfully!  📜 Found 32 paragraphs!  ✅ 28 new paragraphs saved!  ⏳ Execution Time: 3.21 seconds  🔒 Database closed.  

## 🚀 Customization  

- Change `URL` in `scraper.py` 

## ❌ Issues & Fixes  

| Issue | Fix |  

|-----------------|-------------------|  

| `requests.exceptions.ConnectionError` | Check internet / try different URL |  

| `sqlite3.OperationalError: database is locked` | Close database before re-running |  

| No paragraphs found | Ensure site allows scraping |  

## 📧 Need Help?  

Feel free to ask for improvements! 🚀