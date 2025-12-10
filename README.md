# 📚 Book Store Competitor Monitor & Market Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/bookstore-competitor-scraper/blob/main/scraper_analysis.ipynb)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Libraries](https://img.shields.io/badge/Pandas-Seaborn-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

### 🚀 Project Overview
In the competitive e-commerce landscape, data-driven pricing and inventory strategies are essential for profitability.
This project is an end-to-end **Market Intelligence Tool** developed in **Google Colab** to scrape, clean, and analyze competitor data from *Books to Scrape*.

I simulated a real-world scenario where a stakeholder needed an automated solution to monitor a competitor's catalog of **1,000 books** to answer critical business questions regarding pricing efficiency and inventory risk.

### 📂 Repository Structure
* `scraper_analysis.ipynb`: The main notebook containing the scraper logic, data cleaning pipeline, and EDA.
* `books_data.csv`: The final processed dataset (1,000 rows) with clean numerical values for Price, Rating, and Stock.
* `Bookstore_Analysis_Portfolio.pdf`: A PDF export of the analysis including all visualizations.

---

### 🔍 Key Business Insights
After scraping and analyzing the full catalog, I discovered several inefficiencies in the store's strategy:

#### 1. 📉 Pricing Efficiency (Correlation Analysis)
* **Hypothesis:** Does the store charge a premium for higher-quality books?
* **Finding:** Analysis revealed a **near-zero correlation** between Price and Star Rating.
* **Conclusion:** The pricing strategy is inefficient. Customers pay the same average price (£35) for 1-star books as they do for 5-star books, missing an opportunity for premium pricing on high-rated items.

#### 2. 📦 Inventory Risk Management
* **Hypothesis:** Does the store minimize risk by holding less stock of expensive items?
* **Finding:** The correlation between Price and Stock Quantity is **-0.01** (non-existent).
* **Business Risk:** The store holds equal inventory levels for cheap (£10) and expensive (£60) items. This indicates poor working capital management, as capital is tied up in high-cost, potentially slow-moving inventory.

#### 3. 💎 Portfolio Optimization ("Gems" vs. "Mines")
I segmented the inventory to create actionable lists for the marketing team:
* **💎 Hidden Gems:** Identified 5-Star books priced under £20.
    * *Recommendation:* Launch a "Best Value" campaign to drive volume.
* **💣 Risky Mines:** Identified 1-Star books priced over £50.
    * *Recommendation:* Execute a 30% clearance sale to liquidate this dead stock and free up cash flow.

#### 4. 📝 Content Strategy (NLP)
A **Word Cloud** analysis of product titles highlighted a dominance of keywords like *"Life"*, *"Story"*, and *"Love"*, aligning with the category analysis which showed **Fiction** and **Romance** as the top-stocked categories.

---

### 🛠️ Technologies & Methodology

#### 1. Data Collection (Web Scraping)
* **Environment:** Google Colab.
* **Libraries:** `Requests`, `BeautifulSoup`.
* **Technique:** Built a crawler to iterate through 50 pagination pages, extract product links, and "deep dive" into each product page to retrieve specific metadata (Stock count, Category, Exact Rating).

#### 2. Data Cleaning & Transformation
* **Libraries:** `Pandas`, `NumPy`, `RegEx`.
* **Key Steps:**
    * Cleaned currency symbols (`£`, `Â£`) and converted to Float.
    * Extracted integer stock counts from unstructured strings ("In stock (22 available)") using Regex.
    * Mapped textual ratings ("Three") to integers (3).

#### 3. Exploratory Data Analysis (EDA)
* **Libraries:** `Matplotlib`, `Seaborn`, `WordCloud`.
* **Visualizations:** Created Box Plots (Price vs. Rating), Regression Plots (Stock Strategy), and Histograms (Price Distribution) to prove business hypotheses.

---

### 💻 How to Run This Project

You can run the analysis directly in the browser using Google Colab:

1. **Click the "Open in Colab" badge** at the top of this README.
2. **Or run locally:**
   ```bash
   git clone [https://github.com/YourUsername/bookstore-competitor-scraper.git](https://github.com/YourUsername/bookstore-competitor-scraper.git)
   pip install pandas requests beautifulsoup4 seaborn matplotlib wordcloud
   # Open scraper_analysis.ipynb in Google Colab or VS Code

### 👤 Author
Created by Adar Zilbershtein
https://www.linkedin.com/in/adar-zilbershtein/
Feel free to reach out for any questions or collaborations!
